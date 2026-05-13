<div align="center">

# GitHat Inc

**Legal entity for the [GitHat](https://githat.io) identity + hosting platform.**

[**🌐 githat.io**](https://githat.io) · [**💻 Engineering**](https://github.com/GitHat-IO) · [**📦 npx create-githat-app**](https://github.com/GitHat-IO/create-githat-app)

</div>

---

## About this org

This GitHub org is the **legal entity home** for GitHat Inc. Day-to-day engineering work happens in [`GitHat-IO`](https://github.com/GitHat-IO); this org exists to hold:

- 📜 Corporate legal artifacts (data-room, MSAs, DPAs)
- 🔐 Customer-facing security disclosure ([security@githat.io](mailto:security@githat.io))
- 📋 Audit-archive references (SOC 2 CC7.2 WORM bucket)
- 🏗 Cross-platform infrastructure that doesn't belong to a single consumer app

If you're a customer, partner, or auditor: this is the right org.
If you're a contributor or developer: go to [`GitHat-IO`](https://github.com/GitHat-IO).

## The platform

GitHat is the identity + edge platform. Every app delegates auth to `api.githat.io`:

| App | Domain | Engineering org | Legal entity |
|---|---|---|---|
| GitHat | [githat.io](https://githat.io) | [GitHat-IO](https://github.com/GitHat-IO) | **GitHat-Inc** *(this org)* |
| Sebastn | [sebastn.com](https://sebastn.com) | [SebasTN-Rhys](https://github.com/SebasTN-Rhys) | [SebasTN-Inc](https://github.com/SebasTN-Inc) |
| ClickReserv | [reserv.click](https://reserv.click) | [ClickReserv](https://github.com/ClickReserv) | [ClickReserv-Inc](https://github.com/ClickReserv-Inc) |
| Quantl | [quantl.click](https://quantl.click) | [QuantLinc](https://github.com/QuantLinc) | [QuantL-Inc](https://github.com/QuantL-Inc) |
| Colmado | [colmado.click](https://colmado.click) | [Colmado-Inc](https://github.com/Colmado-Inc) | (dual-purpose org) |
| NFTeria | [nfteria.click](https://nfteria.click) | [NFTeria](https://github.com/NFTeria) | [NFTeria-Inc](https://github.com/NFTeria-Inc) |

## Security

- **Disclose vulnerabilities:** [security@githat.io](mailto:security@githat.io) — see [SECURITY.md](./SECURITY.md)
- **Verified domains:** `githat.io` + `www.githat.io` (cert via AWS ACM, CAA-locked)
- **Auth:** RS256 JWTs, AWS KMS-backed signing, JWKS at `/.well-known/jwks.json`
