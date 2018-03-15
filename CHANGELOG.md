# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [vNext]
- Added `StringExtensions.ReplaceRegex` for fluent regular expression replacements.
- Added `[Tool]Tasks.[Tool]Path` property for better accessibility.
- Added `DotCoverTasks` aliases for `cover`, `delete`, `merge`, `report` and `zip`.
- Changed `DotCoverTasks` and `OpenCoverTasks` to use `SetTargetSettings` instead of a delegate.
- Changed `NukeBuild.Configuration` to be overridable but still injectable.
- Changed `StringExtensions.JoinNewLine` to accept `PlatformFamily` parameter which designates line-endings.
- Fixed `ProcessManager` to resolve `toolPath` from environment.
- Fixed `ProcessManager` to filter executable based on operating system and file extensions.
- Fixed line-endings in setup scripts.

## [0.2.10] / 2018-03-05
- Fixed handling of `Graph` switch.
- Fixed logging in Nuke.CodeGenerator.
- Fixed temporary directory path in setup and bootstrapping scripts.
- Fixed `NuGetSettings` to resolve tool path from `NuGet.CommandLine` package.
- Fixed `Invoke-WebRequest` when InternetExplorer's first-launch configuration was not completed.
- Fixed resolution of relative paths to be minimal.
- Fixed `PathConstruction.GetRelativePath` to work with UNIX paths.
- Fixed argument formatting for boolean values.
- Fixed enumeration of modified collection.

## [0.2.0] / 2018-02-26
- Deprecated `Target` parameter in favor of passing targets as first argument to the bootstrapping scripts.
- Deprecated `NoDeps` parameter in favor of new `Skip` parameter that takes a separated list.
- Deprecated `DefaultSettings` which are now exposed in each task class individually.
- Changed default values for `AssemblyVersion` to `{major}.{minor}.0` and `FileVersion` to `{major}.{minor}.{patch}`.
- Added possibility to use `ParameterAttribute` in other injection attributes.
- Added `GitVersionAttribute.Bump` parameter for bumping major/minor versions.
- Added `GitVersionAttribute.DisableOnUnix` property since GitVersion is not working consistently.
- Added `ChangelogTasks.FinalizeChangelog` for finalizing unpublished changes to a certain version.
- Added `ChangelogTasks.ExtractChangelogSectionNotes` for extracting release data for a specified tag.
- Added `NukeBuild.InvokedTargets` which exposes targets passed from command-line.
- Added `NukeBuild.ExecutingTargets` which exposes targets that will be executed.
- Added `NukeBuild.SkippedTargets` which exposes targets that will be skipped.
- Added `GitRepository.IsGitHubRepository` extension method.
- Added `GitRepositoryAttribute.Branch` and `GitRepositoryAttribute.Remote` properties for pass-through.
- Added `build.cmd` in setup for easier invocation on Windows.
- Added CLT tasks for Git.
- Fixed background color in console output.

[vNext]: https://github.com/nuke-build/nuke/compare/0.2.10...HEAD
[0.2.10]: https://github.com/nuke-build/nuke/compare/0.2.0...0.2.10
[0.2.0]: https://github.com/nuke-build/nuke/tree/0.2.0
