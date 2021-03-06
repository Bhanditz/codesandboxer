# Changelog

## 0.4.0

- Rewrote logic that handles parsing imports. As well as just being a bit more secure, it now correctly support:
  - require statements as well as imports
  - `export a from 'b'` syntax

## 0.3.0

BREAKING - fetchFiles now returns just the { files, deps } object, which was previously returned as files. It no longer return parameters or name.
BREAKING - finaliseCSB is now exported. The API for this function has changed dramatically as well. This function accepts the mix of files, deps, and several other passed in values, and is used to generate the parameter hash.

The new workflow goes fetchFiles() -> finaliseCSB() -> sendFilesToCSB, with the ability to put your own logic in between these.

FEATURE - resolvePath is now exported. This is to support codesandboxer-fs, which wants to rely upon it.

## 0.2.2

Use the formData package for deploys instead of the native web formData. This is to allow codesandboxer to be node-compatible.

## 0.2.1

An internal call of `fetchRelativeFile` was not being passed the new 'config' object, causing an error in file fetching. It is now being passed the correct object.

## 0.2.0

Add a new argument to `fetchFiles`, and `fetchRelativeFile` that is a config object.

To the config object add `allowJSX` as a property with a boolean value.

Codesandboxer can now load jsx files if you opt into it.

* allow loading of JSX files
* Add tests using fixtures in repo to test file resolution

## 0.1.1

Stop using \* import due to struggles with transform-runtime

## 0.1.0

Be extracted from react-codesandboxer
