# tree-sitter-lsp

[![readthedocs](https://shields.io/readthedocs/tree-sitter-lsp)](https://tree-sitter-lsp.readthedocs.io)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/Freed-Wu/tree-sitter-lsp/main.svg)](https://results.pre-commit.ci/latest/github/Freed-Wu/tree-sitter-lsp/main)
[![github/workflow](https://github.com/Freed-Wu/tree-sitter-lsp/actions/workflows/main.yml/badge.svg)](https://github.com/Freed-Wu/tree-sitter-lsp/actions)
[![codecov](https://codecov.io/gh/Freed-Wu/tree-sitter-lsp/branch/main/graph/badge.svg)](https://codecov.io/gh/Freed-Wu/tree-sitter-lsp)
[![DeepSource](https://deepsource.io/gh/Freed-Wu/tree-sitter-lsp.svg/?show_trend=true)](https://deepsource.io/gh/Freed-Wu/tree-sitter-lsp)

[![github/downloads](https://shields.io/github/downloads/Freed-Wu/tree-sitter-lsp/total)](https://github.com/Freed-Wu/tree-sitter-lsp/releases)
[![github/downloads/latest](https://shields.io/github/downloads/Freed-Wu/tree-sitter-lsp/latest/total)](https://github.com/Freed-Wu/tree-sitter-lsp/releases/latest)
[![github/issues](https://shields.io/github/issues/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/issues)
[![github/issues-closed](https://shields.io/github/issues-closed/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/issues?q=is%3Aissue+is%3Aclosed)
[![github/issues-pr](https://shields.io/github/issues-pr/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/pulls)
[![github/issues-pr-closed](https://shields.io/github/issues-pr-closed/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/pulls?q=is%3Apr+is%3Aclosed)
[![github/discussions](https://shields.io/github/discussions/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/discussions)
[![github/milestones](https://shields.io/github/milestones/all/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/milestones)
[![github/forks](https://shields.io/github/forks/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/network/members)
[![github/stars](https://shields.io/github/stars/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/stargazers)
[![github/watchers](https://shields.io/github/watchers/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/watchers)
[![github/contributors](https://shields.io/github/contributors/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/graphs/contributors)
[![github/commit-activity](https://shields.io/github/commit-activity/w/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/graphs/commit-activity)
[![github/last-commit](https://shields.io/github/last-commit/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/commits)
[![github/release-date](https://shields.io/github/release-date/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/releases/latest)

[![github/license](https://shields.io/github/license/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp/blob/main/LICENSE)
[![github/languages](https://shields.io/github/languages/count/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp)
[![github/languages/top](https://shields.io/github/languages/top/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp)
[![github/directory-file-count](https://shields.io/github/directory-file-count/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp)
[![github/code-size](https://shields.io/github/languages/code-size/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp)
[![github/repo-size](https://shields.io/github/repo-size/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp)
[![github/v](https://shields.io/github/v/release/Freed-Wu/tree-sitter-lsp)](https://github.com/Freed-Wu/tree-sitter-lsp)

[![pypi/status](https://shields.io/pypi/status/tree-sitter-lsp)](https://pypi.org/project/tree-sitter-lsp/#description)
[![pypi/v](https://shields.io/pypi/v/tree-sitter-lsp)](https://pypi.org/project/tree-sitter-lsp/#history)
[![pypi/downloads](https://shields.io/pypi/dd/tree-sitter-lsp)](https://pypi.org/project/tree-sitter-lsp/#files)
[![pypi/format](https://shields.io/pypi/format/tree-sitter-lsp)](https://pypi.org/project/tree-sitter-lsp/#files)
[![pypi/implementation](https://shields.io/pypi/implementation/tree-sitter-lsp)](https://pypi.org/project/tree-sitter-lsp/#files)
[![pypi/pyversions](https://shields.io/pypi/pyversions/tree-sitter-lsp)](https://pypi.org/project/tree-sitter-lsp/#files)

A core library to support language servers.

I write many language servers and they share some same code so I extract the
shared code to this library.

I've had enough of writing many DSLs in my editor without any LSP support
(completion, hover, ...). So I decide to sacrifice my time to do this work.
Some [Chinese blogs](https://freed-wu.github.io/tag/lsp/) about how I write
these language servers.

## Language servers

### Use tree-sitter and json schema

- [termux-language-server](https://github.com/termux/termux-language-server/):
  for some specific bash scripts:
  - [`build.sh`](https://github.com/termux/termux-packages/wiki/Creating-new-package)
  - [`PKGBUILD`](https://wiki.archlinux.org/title/PKGBUILD)
  - [`*.ebuild`](https://dev.gentoo.org/~zmedico/portage/doc/man/ebuild.5.html)
  - ...
- [zathura-language-server](https://github.com/Freed-Wu/zathura-language-server):
  for [zathura](https://github.com/pwmt/zathura)'s zathurarc

### Use tree-sitter

- [requirements-language-server](https://github.com/Freed-Wu/requirements-language-server/):
  for `requirements.txt`
- [autotools-language-server](https://github.com/Freed-Wu/autotools-language-server/):
  for `Makefile`

### Don't use tree-sitter

- [mutt-language-server](https://github.com/neomutt/mutt-language-server):
  for [(neo)mutt](https://github.com/neomutt/neomutt)'s (neo)muttrc
- [bitbake-language-server](https://github.com/Freed-Wu/bitbake-language-server):
  for [bitbake](https://docs.yoctoproject.org/bitbake/index.html)
- [tmux-language-server](https://github.com/Freed-Wu/tmux-language-server):
  for [tmux](https://github.com/tmux/tmux)'s `tmux.conf`
- [sublime-syntax-language-server](https://github.com/Freed-Wu/sublime-syntax-language-server):
  for sublime syntax's test file `syntax_test_*`
- [expect-language-server](https://github.com/Freed-Wu/expect-language-server):
  for [expect](https://wiki.tcl-lang.org/page/Expect)
- [xilinx-language-server](https://github.com/Freed-Wu/xilinx-language-server):
  for xilinx's xsdb, xsct
- [translate-shell](https://github.com/Freed-Wu/translate-shell):
  translate the word under the cursor

## What does this library provide

### Finders

Some finders to find the required node in tree-sitter's AST.
Such as, if you want to get the node under the cursor:

```python
@self.feature(TEXT_DOCUMENT_COMPLETION)
def completions(params: CompletionParams) -> CompletionList:
    document = self.workspace.get_document(params.text_document.uri)
    uni = PositionFinder(params.position, right_equal=True).find(
        document.uri, self.trees[document.uri]
    )
    # ...
```

UNI (Universal Node Identifier) is URI + node.

### Schema

A `Trie` to convert a file to a json, then you can use json schema to validate
it to get diagnostics.

Take
[termux-language-server](https://github.com/termux/termux-language-server/) as
an example. This is a `PKGBUILD`:

```sh
pkgname=hello
pkgver=0.0.1
pkgrel=1
pkgdesc="hello"
arch=(any)
license=(GPL3)

build() {
    cat <<EOF > hello
#!/usr/bin/env sh
echo hello
EOF
}

package() {
    install -D hello -t $pkgdir/usr/bin
}
```

```sh
termux-language-server --convert PKGBUILD
```

```json
{
  "pkgname": "hello",
  "pkgver": "0.0.1",
  "pkgrel": "1",
  "pkgdesc": "hello",
  "arch": [
    "any"
  ],
  "license": [
    "GPL3"
  ],
  "build": 0,
  "package": 0
}
```

So, we can validate the json by a json schema. For termux-language-server,
these json schemas are
[here](https://github.com/termux/termux-language-server/tree/main/src/termux_language_server/assets/json).

### Utilities

This library still provide many utility functions. Such as convert man page to
markdown and tokenize it in order to generate the json schema.

## References

- [tree-sitter](https://tree-sitter.github.io/tree-sitter/)
- [language server protocol](https://microsoft.github.io/language-server-protocol/specifications/specification-current)
- [json schema](https://json-schema.org/specification)
