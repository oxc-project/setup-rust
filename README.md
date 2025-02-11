```yaml
- uses: oxc-project/setup-rust@cd82e1efec7fef815e2c23d296756f31c7cdc03d # v1.0.0
  with:
    # warm cache factory for all other CI jobs
    # cache `target` directory to avoid download crates
    save-cache: ${{ github.ref_name == 'main' }}
    cache-key: warm
    tools: just,cargo-shear@1,dprint
    components: clippy rustfmt
```
