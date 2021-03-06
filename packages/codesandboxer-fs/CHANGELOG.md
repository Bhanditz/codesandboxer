# Changelog

## 0.3.0

Using 0.4 of codesandboxer, leading to better analysis of imports/exports and support for parsing requires
Add a `name` flag that allows you to set the sandbox's name
Add an `allowedExtensions` flag that allows extensions to be provided (for example '.jsx')
If the entry file is of a different file type, automatically add that file type to the allowed extensions.

## 0.2.1

Actually fix bug with path resolution.

## 0.2.0

Using v0.3 of codesandboxer - API changes that have made fs work much more nicely
with codesandboxer.
dry flag is now '--dry, -D' instead of '--dry, -d' (this has been made so -d can be used with dependencies)
Added '--name' flag, which allows you to name your sandbox
Fixed a bug with path resolution that would lead to trying to access non-existent files

## 0.1.0

Fixed a pernicious bug, changed how things work, vote of confidence bump.

## 0.0.2

Added documentation

## 0.0.1

Initial Release. Very unstable, do not rely upon it.
