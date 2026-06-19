# IXO DID Method (`did:ixo`)

This repository contains the specification for the `did:ixo` Decentralized Identifier method,
an implementation of the Interchain Identifier (IID) framework anchored on the IXO blockchain.

## Specification

The specification is located at:

```
interchain-identifiers/v1.md
```

It defines the `did:ixo` method, which builds on the
[W3C DID Core specification](https://www.w3.org/TR/did-core/) and the Interchain Identifier (IID)
framework originally developed in partnership with the Interchain Foundation.

**Upstream source:** The IID v1 specification was originally published at:
https://github.com/ixofoundation/ixo-protocol/blob/7ee90538b8a01dc3f696c190af62f2f39a866d9d/interchain-identifiers/v1.md

## Quick Reference

| Property          | Value                                                      |
|-------------------|------------------------------------------------------------|
| **Method name**   | `ixo`                                                      |
| **DID prefix**    | `did:ixo:`                                                 |
| **DID example**   | `did:ixo:entity:abc123`                                    |
| **Registry**      | IXO Blockchain (Cosmos SDK)                                |
| **Status**        | Draft — pending W3C registry submission                    |
| **JSON-LD context** | `https://w3id.org/ixo/ns/interchain-identifiers/v1`    |

## Key Features

- **IID extensions**: Linked Resources, Accorded Rights, Polymorphic Mediators, and more
- **Privacy-preserving**: Hashgraph proofs obscure the quantity and content of linked resources
- **Herd privacy**: Single-mediator pattern to prevent subject identification by endpoint
- **Interchain**: Compatible with the IID family of DID methods across Cosmos chains
- **zCap support**: Authorization Capabilities (zCaps) for capability delegation and invocation

## W3C Registry Submission

Submission materials are in the `submission/` directory:

- `submission/ixo.json` — Registry entry JSON (copy to `methods/` in `w3c/did-spec-registries`)
- `submission/self-assessment.md` — Completed self-assessment checklist

See `submission/self-assessment.md` for step-by-step submission instructions.

## Implementations

- **IXO Blockchain**: https://github.com/ixofoundation/ixo-blockchain
- **IXO Multiclient SDK**: https://github.com/ixofoundation/ixo-multiclient-sdk
- **IXO Impact Client SDK**: https://www.npmjs.com/package/@ixo/impactxclient-sdk

## DID Resolution

Resolve a `did:ixo` DID using the IXO blockchain REST or gRPC API:

```bash
# REST (replace with your IXO node endpoint)
curl https://rpc.ixo.earth/ixo/iid/v1beta1/iidDocuments/did:ixo:entity:abc123
```

## License

This specification is published under the
[W3C Software and Document License](https://www.w3.org/Consortium/Legal/2015/copyright-software-and-document).
