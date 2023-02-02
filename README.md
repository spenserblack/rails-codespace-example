# Rails Codespace Example

This repository is mostly the end result of following the
[Getting Started with Rails][tutorial] tutorial. However,
it also includes some configuration to support developing in
a GitHub Codespace. [PR #1][codespaces-pr] shows the changes
made in order to make it easier to develop in a codespace.

- The Codespace uses Ruby2.7
- `bundle install` is run when the codespace is first created
- Whenever you connect to the codespace, the database is migrated and the rails server starts
- *Only when you're in a codespace* (detected by the `CODESPACES` environment variable),
  the preview domain will be added to the allowed hosts.
- port 3000 is forwarded to use that preview domain.
- The Ruby version in the Gemfile is made less strict, due to codespaces installing `2.7.7`.
- Miscellaneous
  - The EditorConfig extension is installed, and an `.editorconfig` file is added to keep
    behavior between editors consistent.

[tutorial]: https://guides.rubyonrails.org/getting_started.html
[codespaces-pr]: https://github.com/spenserblack/rails-codespace-example/pull/1
