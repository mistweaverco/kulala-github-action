<div align="center">

![Kulala Logo](logo.svg)

# kulala-github-action

[![Made with love][badge-made-with-love]][contributors]
[![Discord][badge-discord]][discord]
[![Development status][badge-development-status]][development-status]
[![Our manifesto][badge-our-manifesto]][our-manifesto]
[![AI Policty][badge-ai-policy]][ai-policy]

[Usage](https://kulala.app/usage) •

<p></p>

# Other tools 🔧 from the Kulala 🐼 family 🧑‍🧑‍🧒‍🧒

[Kulala for Neovim][kulala.nvim] •
[Kulala CLI][kulala-cli] •
[Kulala Formatter (and converter)][kulala-fmt] •
[Kulala Desktop][kulala-desktop] •
[Kulala for Visual Studio Code][kulala.vscode] •
[Kulala Core][kulala-core]

---

</div>

## Usage

Kulala provides a Github Action to run HTTP files as
part of your CI/CD pipeline.

Example:
```yaml
---
name: main
on:
  pull_request: ~
jobs:
  build:
    name: Run HTTP tests
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repo
        uses: actions/checkout@v6

      - name: Setup Kulala CI
        uses: mistweaverco/kulala-github-action@v1

      - name: Run Kulala CI
        run: |
          # Run all .http files in the http-files/ directory
          # and only output if there are test failures
          kulala run http-files/ --tests --quiet
```



[badge-discord]: https://mistweaverco.com/assets/badges/discord.svg
[discord]: https://mistweaverco.com/discord
[badge-made-with-love]: https://mistweaverco.com/assets/badges/made-with-love.svg
[contributors]: https://github.com/mistweaverco/kulala-github-action/graphs/contributors
[kulala-cli]: https://github.com/mistweaverco/kulala-cli
[kulala-fmt]: https://github.com/mistweaverco/kulala-fmt
[kulala-desktop]: https://github.com/mistweaverco/kulala-desktop
[kulala.vscode]: https://github.com/mistweaverco/kulala.vscode
[kulala-core]: https://github.com/mistweaverco/kulala-core
[kulala.nvim]: https://github.com/mistweaverco/kulala.nvim
[demo-image]: https://github.com/user-attachments/assets/a7b3b01f-0115-44dc-94d2-8abd4db6fb60
[badge-development-status]: https://mistweaverco.com/assets/badges/development-status.svg
[development-status]: https://mistweaverco.com/roadmap?filter=kulala-github-action
[badge-ai-policy]: https://mistweaverco.com/assets/badges/ai-policy.svg
[ai-policy]: https://mistweaverco.com/ai-policy
[badge-our-manifesto]: https://mistweaverco.com/assets/badges/our-manifesto.svg
[our-manifesto]: https://mistweaverco.com/manifesto
