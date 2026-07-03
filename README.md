```yaml
- uses: oxc-project/setup-rust@cd82e1efec7fef815e2c23d296756f31c7cdc03d # v1.0.0
  with:
    # warm cache factory for all other CI jobs
    # cache `target` directory to avoid download crates
    save-cache: ${{ github.ref_name == 'main' }}
    cache-key: warm
    tools: just,cargo-shear@1.13.1,dprint
    components: clippy rustfmt
```

## ❤ Who's [Sponsoring Oxc](https://github.com/sponsors/Boshen)?

<p align="center">
  <a href="https://github.com/sponsors/Boshen">
    <img src="https://raw.githubusercontent.com/Boshen/sponsors/main/sponsors.svg" alt="Our sponsors" />
  </a>
</p>
