# Changelog

See the full list of recent releases and features added on the
[Github releases page](https://github.com/PranayAgarwal/vscode-hack/releases).

## v2.20.0 - 2024-04-24

- Update comment syntax (from `#` to `//`) in snippets. Thanks [Glitched](https://github.com/Glitched)!

## v2.19.0 - 2024-03-05

- New status bar indicator for LSP -> hh_server connectivity issues.

## v2.18.0 - 2024-02-29

- New autocomplete helpers for JSDoc comment blocks (`/** ... */`).
- Removed `onDebug` as an activation event to prevent unnecessary extension activations.

## v2.17.1 - 2023-07-10

- Automated and manual security fixes for dependencies.
- Minor project housekeeping:
  - Updated some package paths (`vscode-debugadapter`, `vscode-debugprotocol` and `vsce` all moved under the `@vscode` npm org).
  - Added some required OSS notices to the repo.

## v2.16.0 - 2022-10-03

- Syntax highlighting fixes. Thanks [Wilfred](https://github.com/Wilfred) & [panopticoncentral](https://github.com/panopticoncentral)!

## v2.15.0 - 2022-09-27

- Syntax highlighting for await and concurrent. Thanks [Wilfred](https://github.com/Wilfred)!
- Syntax highlighting for modules. Thanks [panopticoncentral](https://github.com/panopticoncentral)!

## v2.14.0 - 2022-08-25

- Lots of syntax highlighting fixes. Thanks [Wilfred](https://github.com/Wilfred)!
- Fix file path mappings on Windows. Thanks [skoro](https://github.com/skoro)!

## v2.13.0 - 2022-03-09

- Removed custom workspace trust mechanism, since VS Code now has it built-in (thanks
  [@fredemmott](https://github.com/fredemmott))!
- Automated publishing of extension package as a release asset.

## v2.12.0 - 2021-10-28

- Reverted expression-trees syntax highlighting rule due to performance issues.
- Removed error suppression code action.

## v2.11.0 - 2021-09-30

- Syntax highlighting improvements. Thanks
  [Wilfred](https://github.com/Wilfred)!
- Hack error suppression action in LSP mode. Thanks
  [icechen1](https://github.com/icechen1)!
- `#region` folding support. Thanks [turadg](https://github.com/turadg)!

## v2.10.0 - 2020-08-18

- Auto-start Hack typechecker on workspace load. Thanks
  [antoniodejesusochoasolano](https://github.com/antoniodejesusochoasolano)!
- Syntax highlighting improvements

## v2.9.7 - 2020-08-18

- Syntax highlighting fix (adding missed `Pair` literal).

## v2.9.6 - 2020-08-15

- Syntax highlighting improvements. Thanks
  [Wilfred](https://github.com/Wilfred)!

## v2.9.5 - 2020-05-19

- Updated snippets
- Remove build badge from README

## v2.9.4 - 2020-03-02

- Fix for "Invalid variable attributes" error in debugger panel when stopped on
  a breakpoint.

## v2.9.3 - 2020-01-30

- Syntax highlighting fixes
- Remove deprecated PHP snippets

## v2.9.2 - 2019-12-17

- Fix `NOTICE.md` file, which was accidentally left blank in the last release.

## v2.9.1 - 2019-12-16

- Better error messages when `hh_client` connection fails and extension is
  running in remote mode (using either SSH or Docker). Thanks
  [icechen1](https://github.com/icechen1)!

## v2.9.0 - 2019-11-22

- New `launchUrl` option in debugger attach config automatically invokes a web
  request once the debugger is attached, and detaches when the request is
  complete.

## v2.8.1 - 2019-11-10

- Syntax highlighting improvements. Thanks
  [scotchval](https://github.com/scotchval)!

## v2.8.0 - 2019-10-30

- If the IDE session is connected to a remote typechecker of type `docker`,
  scripts run via the launch debug target now automatically start in the Docker
  container instead of the host machine. Stopping on breakpoints isn’t yet
  supported in this mode.

## v2.7.1 - 2019-10-28

- Syntax highlighting fixes. Thanks [lildude](https://github.com/lildude)!

## v2.7.0 - 2019-10-17

- Lots of syntax highlighting updates. Thanks
  [tspence](https://github.com/tspence)!

## v2.6.0 - 2019-09-16

- Config values now support the `${workspaceFolder}` variable.

## v2.5.1 - 2019-07-26

- Fix — in later HHVM versions the LSP doesn't send over connection status, so
  hide the status bar indicator for those cases.

## v2.5.0 - 2019-07-25

- Added a connection indicator in the editor status bar which shows HHVM version
  & LSP status/errors. This should make it easier to debug problems in IDE
  functionality related to hh_server crashes or restarts.

## v2.4.1 - 2019-07-23

- Bug fixes in coverage checker
- Syntax highlighting updates

## v2.4.0 - 2019-05-15

- Add support for Unix domain sockets for debugger "attach" target.

## v2.3.0 - 2019-05-06

- Show modal asking users to reload the workspace on changes to `hack.remote.*`
  configuration settings.

## v2.2.0 - 2019-04-22

- **Syntax Highlighting Updates** — Support for `__dispose`, `__disposeAsync`,
  `newtype` and `async`.

## v2.1.0 - 2019-03-08

- **Syntax Highlighting Updates** — Editor will now recognize `arraykey`,
  `nonnull`, `dict`, `vec` and `keyset` as valid storage types.

## v2.0.0 - 2019-03-06

- **Remote language server connection support** — You can now connect to an
  external development environment for Hack typechecking, linting and all other
  intellisense features. Current supported methods are SSH and Docker. See the
  **Remote Development** section in README.md for more details.
  - This version may cause breaking changes to your existing setup if you were
    already using Docker via a custom `hack.clientPath` executable.
  - The `hack.workspaceRootPath` config has been renamed to
    `hack.remote.workspacePath`.
- Running the extension with LSP mode disabled is now unsupported. It will be
  fully removed in a future version of the extension.

## v1.2.1 - 2019-02-19

- Fixed [#40](https://github.com/slackhq/vscode-hack/issues/40) — Syntax
  highlighting breaks for `.hack` files that contain `<?hh`.

## v1.2.0 - 2019-02-12

- **Support for `.hack` files** — VS Code will automatically classify files with
  the `.hack` extension as Hack, and these files will now syntax highlight
  correctly even without the `<?hh` opener. (`.hack` files are supported in HHVM
  4.0.0 onward, so you will see typechecker errors if you are using them with an
  earlier version).

## v1.1.0 - 2018-11-12

- Moved project repository to https://github.com/slackhq org and added required
  notices and docs
- Enabled LSP request tracing for hhast-lint
- Fixed typo in hhast-lint security prompt text
- Language syntax now tracks
  [atom-ide-hack](https://github.com/hhvm/atom-ide-hack) project

## v1.0.1 - 2018-07-26

- Add automatic LSP request tracing via new `hack.tracing.server` config option
  (thanks [@auchenberg](https://github.com/auchenberg)!)

## v1.0.0 - 2018-07-19

- **Integration with HHAST Linter** (thanks
  [@fredemmott](https://github.com/fredemmott)!). The extension now supports
  Hack linting and autofixing via [HHAST](https://github.com/hhvm/hhast/)
  (v3.27.2 or later required). Set up linting for your project by following
  instructions in the HHAST library, then look at workspace-specific linter
  settings in the extension Configuration section.
- Type coverage now uses the language server
- [Fix] Output panel will no longer automatically steal focus on extension
  errors

## v0.8.5 - 2018-07-09

- Only send LSP requests for documents with `file://` scheme
- Send LSP initializtion option to use text edit autocomplete (fixes broken
  variable completion)

## v0.8.4 - 2018-06-04

- Syntax highlighting for `.hhconfig` file
- Added support for showing related messages for an error when running in
  non-LSP mode

## v0.8.3 - 2018-05-30

- Fixed bug in debug launch mode to correctly recognize extra args passed to
  HHVM

## v0.8.2 - 2018-05-28

- Documents are now recognized as Hack if they start with a shebang pointing to
  an HHVM executable (e.g. `#!/usr/bin/hhvm`), regardless of extension
- Debugger bug fixes (stop debug session from getting stuck on bad socket
  connection, copy configuration snippet templates correctly)

## v0.8.1 - 2018-05-14

- Updated Hack language syntax to the latest version
- Removed some unnecessary PHP snippets
- Fixed file path mapping in typechecker requests & responses to use the correct
  scheme (thanks [@fredemmott](https://github.com/fredemmott) for the thorough
  investigation)

## v0.8.0 - 2018-05-10

- **HHVM Debugger (Alpha version)** — Launch scripts or attach to an HHVM server
  straight from VS Code. See the
  [debugger doc](https://github.com/PranayAgarwal/vscode-hack/blob/master/docs/debugging.md)
  for details on setup and usage. _This is a very early release. Please file any
  bugs at the Issues page._
- Hack coverage check works again. A new icon in the editor status bar shows %
  coverage for the file and can be clicked to highlight uncovered areas. (Can be
  disabled by setting `"hack.enableCoverageCheck": false`)

## v0.7.0 - 2018-01-25

- Language Server mode is now on by default for users running HHVM 3.23 or
  later. Add `"hack.useLanguageServer": false` to your workspace config to
  disable it.

## v0.6.2 - 2017-11-20

- Extend Language Server mode support to containerized typechecker instances as
  well.

## v0.6.1 - 2017-11-19

- Patch to include "vscode-languageclient" package in `dependencies` section
  rather than `devDependencies`.

## v0.6.0 - 2017-11-19

- Experimental Language Server support:
  - If you are running HHVM 3.23 or later, add `"hack.useLanguageServer": true`
    to your workspace config to start hh_client in Language Server mode (see
    [#15](https://github.com/PranayAgarwal/vscode-hack/issues/15) for more
    context).
- Support for running against a containerized Hack typecheck server (see Docker
  section in README). Thanks [@beatscode](https://github.com/beatscode)!
- Fixed [#13](https://github.com/PranayAgarwal/vscode-hack/issues/13) - Running
  formatter removes last line of file if there is no trailing newline. Thanks
  [@beefsack](https://github.com/beefsack)!
- Updated Hack language grammar to latest version.
- Development changes:
  - Bumped up minimum supported VS Code engine version to 1.15.0 for better
    extension API compatibility.
  - Project is now compiled in TypeScript strict mode.

## v0.5.0 - 2017-04-06

- Added Code Actions to automatically suppress typechecker errors via HH_FIXME
  comments.

## v0.4.0 - 2017-03-24

- Fixed document symbol outline (⇧⌘O) break in newer hh_client versions.
- Added a new setting to enable type coverage checking (now off by default).
- Updated Hack grammar for better syntax highlighting.
- Lots of performance improvements, mainly by refactoring the codebase to use
  async/await.
- Works best with HHVM 3.18 or later.

## v0.2.2 - 2016-11-07

- Added error code to typechecker messages.
- Minor autocomplete updates:
  - Triggers on namespace segment (\\).
  - Recognizes constructors correctly.

## v0.2.1 - 2016-10-18

- Added ability to toggle Hack coverage highlighting from percentage indicator
  in status bar.
- Added workspace symbol search functionality.
- Updated Hack grammar to latest version (from Nuclide repository).

## v0.1.2 - 2016-10-18

- Added support for custom hh_client path.
- Fixed incorrect namespace suggestion in autocomplete.

## v0.1.1 - 2016-10-13

- Updated extension icon and README file.

## v0.1.0 - 2016-10-13

- Very early in development release of Hack for Visual Studio Code.
