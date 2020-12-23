% erl-uri changelog

# Next Version
## Features
- Export `parse_query` functions which allow to parse `www-form-urlencoded`.
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
