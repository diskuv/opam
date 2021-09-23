Working version changelog, used as a base for the changelog and the release
note.
Possibly scripts breaking changes are prefixed with ✘.
New option/command/subcommand are prefixed with ◈.

## Version
  *

## Global CLI
  *

## Plugins
  *

## Init
  *

## Config report
  *

## Install
  *

## Remove
  *

## Switch
  *

## Pin
  *

## List
  *

## Show
  *

## Var
  *

## Option
  *

## Lint
  *

## Lock
  *

## Opamfile
  *

## External dependencies
  *

## Sandbox
  *

## Repository management
  *

## VCS
  *

## Build
  *

## Infrastructure
  *

## Admin
  *

## Opam installer
  *

## State
  *

# Opam file format
  *

## Solver
  *

## Client
  *

## Internal
  * Generalise `mk_tristate_opt` to `mk_state_opt` [#4575 @rjbou]
  * Fix `mk_state_opt` and rename to `mk_enum_opt` [#4626 @rjbou]
  * Add `mk_enum_opt_all` for state flags that appears more than once [#4582 @rjbou]
  * Fix `opam exec` on native Windows when calling cygwin executables [#4588 @AltGr]
  * Fix temporary file with a too long name causing errors on Windows [#4590 @AltGr]
  * CLI: Add flag deprecation and replacement helper [#4595 @rjbou]
  * Win32 Console: fix VT100 support [#3897 #4710 @dra27]
  * Tidied the opam files [#4620 @dra27]
  * Externalise cli versioning tools from `OpamArg` into `OpamArgTools` [#4606 @rjbou]
  * Each library defines its own environment variables, that fills the config record [#4606 @rjbou]
  * Harden cygpath wrapper [#4625 @dra27]
  * Reset the plugin symlinks when the root is upgraded [#4641 @dra27 - partial fix for #4619]
  * Formalise opam dev version detection with `OpamVersion.is_dev_version` [#4665 @dra27]
  * Add `OpamStd.String.is_prefix_of` [#4694 @rjbou @dra27]
  * Fix `OpamStd.Format.pretty_list`: `last` argument dropped if list contains more than 2 elements [#4694 @rjbou]
  *
  * Add license and lowerbounds to opam files [#4714 @kit-ty-kate]
  * Bump version to 2.2.0~alpha~dev [#4725 @dra27]
  * Support MSYS2: two-phase rsync on MSYS2 to allow MSYS2's behavior of copying rather than symlinking [#4817 @jonahbeckford]

## Internal: Windows
  * Support MSYS2: treat MSYS2 and Cygwin as equivalent [#4813 @jonahbeckford]
  * Process control: close stdin by default for Windows subprocesses and on all platforms for the download command [#4615 @dra27]
  * [BUG] handle converted variables correctly when no_undef_expand is true [#4811 @timbertson]
  * Environment: translate PATH from Windows to Unix during opam env. [#4844 @jonahbeckford]

## Test
  *

## Shell
  *

## Doc
  *

## Security fixes
  *
