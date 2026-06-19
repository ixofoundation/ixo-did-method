# W3C DID Method Registry Self-Assessment — `did:ixo`

This self-assessment accompanies the submission of the `did:ixo` DID method to the
[W3C DID Extensions registry](https://www.w3.org/TR/did-extensions/).

---

## Checklist

### Specification Completeness

- [x] The specification defines a **method name** (`ixo`) — Section 2
- [x] The specification defines **method-specific DID syntax** with ABNF grammar — Section 2
- [x] The specification defines the **Create** operation — Section 5.1
- [x] The specification defines the **Read** (Resolve) operation — Section 5.2 and Section 6
- [x] The specification defines the **Update** operation — Section 5.3
- [x] The specification defines the **Deactivate** operation — Section 5.4
- [x] The specification includes **Security Considerations** — Section 7
- [x] The specification includes **Privacy Considerations** — Section 8
- [x] The specification includes a **Conformance** section — Section 1
- [x] The specification is publicly accessible at a stable URL

### Conformance with DID Core

- [x] IXO DIDs conform to the DID Core syntax (`did:ixo:<method-specific-id>`)
- [x] IXO DID Documents are conformant DID Documents in JSON-LD representation
- [x] The method uses the `@context` property with `https://www.w3.org/ns/did/v1` as the first value
- [x] IXO extension terms are defined by the DID-specific context at `https://w3id.org/ixo/ns/did/v1`
- [x] Verification Methods and Verification Relationships follow DID Core definitions
- [x] Service endpoints follow DID Core definitions
- [x] DID Document Metadata fields (`created`, `updated`, `deactivated`) follow DID Core definitions

### Security

- [x] The specification identifies cryptographic key security requirements
- [x] The specification identifies blockchain network security dependencies
- [x] The specification identifies JSON-LD context integrity requirements
- [x] The specification identifies residual risks (Sybil, correlation, phishing, key loss)

### Privacy

- [x] The specification addresses on-chain data permanence
- [x] The specification recommends content identifiers, hashes, encrypted references, and mediator services for sensitive data
- [x] The specification describes resolver and service-endpoint correlation risks
- [x] The specification addresses correlation risks
- [x] The specification addresses personal data considerations

### Intellectual Property

- [ ] The submitter affirms that the specification does not impose copyright, trademark, or IP
      concerns on W3C, DID Method implementers, or users.
- [ ] Any known IP concerns are authorized under an F/RAND license.

---

## Evidence of Conformance

### Implementation

The `did:ixo` method is implemented in the IXO blockchain's IID module:

- **IXO Blockchain (Cosmos SDK)**: https://github.com/ixofoundation/ixo-blockchain
- **IXO Multiclient SDK**: https://github.com/ixofoundation/ixo-multiclient-sdk
- **IXO Impact Client SDK**: https://www.npmjs.com/package/@ixo/impactxclient-sdk

### Resolver

IXO DID Documents can be resolved via:

- **gRPC**: `ixo.iid.v1beta1.Query/IIDDocument`
- **REST**: `GET /ixo/did/dids/{id}`

### DID Method Rubric

A full evaluation against the [W3C DID Method Rubric](https://w3c.github.io/did-rubric/) is
recommended prior to final submission and should be appended here.

---

## Submission Instructions

To submit the `did:ixo` method to the W3C DID Specification Registries:

1. Fork https://github.com/w3c/did-extensions
2. Copy `submission/ixo.json` to the `methods/` directory of the forked repo
3. Confirm the `"specification"` URL points to the public canonical README
4. Open a Pull Request with a completed self-assessment checklist
5. Await review by at least two registry maintainers
6. Respond to any feedback within the 7-day minimum review period
