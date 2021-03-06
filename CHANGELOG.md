% erl-uri changelog

# Next Version
## Changes
- `uri_paths:join/1` now accept absolute path segments. Absolute paths in the
  segment list are technically incorrect, but the convenience of being able to
  join recursively is worth it.

# 1.3.0
## Features
- Add new functions to access and modify uri query parameters:
  - `uri:query_parameter/2`;
  - `uri:query_parameter/3`;
  - `uri:find_query_parameter/2`;
  - `uri:has_query_parameter/2`;
  - `uri:add_query_parameter/3`;
  - `uri:add_query_parameters/2`;
  - `uri:remove_query_parameter/2`;
  - `uri:remove_query_parameters/2`.
- Add `uri:encode_query/1` which can be useful out of uris, e.g. for HTML form
  data.
- Add `uri_paths:join/1` to facilitate path construction.
## Changes
- The square brackets used to delimit IPv6 addresses in host parts are now
  removed during parsing, and added during serialization.

# 1.2.2
## Features
- Export `uri:encode_path/1`.
## Bug fixes
- Fix query encoding.

# 1.2.1
## Features
- Add `uri:parse_query/1` since it can also be used to parse
  `www-form-urlencoded` data.
- Add an `uri:error_reason/0` type.
- Add `uri:format_error/1` to return human-readable error strings.
## Bug fixes
- `uri:resolve_reference/2` should signal an error instead of throwing one.

# 1.2.0
## Features
- Add URI accessors: `uri:path/1`, `uri:query/1`, `uri:fragment/1`.
## Misc
- Use result tuples for parsing and decoding, instead of signaling errors. For
  example, `uri:parse/1` now returns either `{ok, URI}` or `{error, Reason}`
  instead of either return a URI or signaling an error.

# 1.1.0
## Features
- Do not serialize empty queries and fragments.

# 1.0.0
First public version.
