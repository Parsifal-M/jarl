# Jarl

The _JVM Alternative for the Rego Language_ (JARL) is an OPA evaluator for the JVM, written in Clojure.

## Usage

FIXME

## Supported built-in functions

### Comparison

- [x] `==`
- [x] `!=`
- [x] `<`
- [x] `<=`
- [x] `>`
- [x] `>=`

### Numbers

- [x] `+`
- [x] `-`
- [x] `*`
- [x] `/`
- [x] `%`
- [x] `round`
- [x] `ceil`
- [x] `floor`
- [x] `abs`
- [x] `numbers.range`
- [ ] `rand.intn`

### Aggregates

- [x] `count`
- [x] `sum`
- [x] `product`
- [x] `max`
- [x] `min`
- [x] `sort`

### Arrays

- [x] `array.concat` 
- [x] `array.reverse`
- [x] `array.slice`

### Sets

- [x] `&`
- [x] `|`
- [x] `-`
- [x] `intersection`
- [x] `union`

### Objects

- [x] `object.get`
- [x] `object.remove`
- [x] `object.union`
- [x] `object.union_n`
- [x] `object.filter`
- [ ] `json.filter`
- [ ] `json.remove`
- [ ] `json.patch`

### Strings

- [x] `concat`
- [x] `contains`
- [x] `endswith`
- [x] `format_int`
- [x] `indexof`
- [x] `indexof_n`
- [x] `lower`
- [x] `replace`
- [x] `strings.reverse`
- [ ] `strings.replace_n`
- [x] `split`
- [ ] `sprintf`
- [x] `startswith`
- [x] `substring`
- [x] `trim`
- [x] `trim_left`
- [x] `trim_prefix`
- [x] `trim_right`
- [x] `trim_suffix`
- [x] `trim_space`
- [x] `upper`

### Regex

https://github.com/google/re2j

- [x] `regex.match`
- [x] `regex.is_valid`
- [x] `regex.split`
- [ ] `regex.globs_match`
- [ ] `regex.template_match`
- [x] `regex.find_n`
- [ ] `regex.find_all_string_submatch_n`

### Glob

- [ ] `glob.match`
- [ ] `glob.quote_meta`

### Bitwise

- [x] `bits.or`
- [x] `bits.and`
- [x] `bits.negate`
- [x] `bits.xor`
- [x] `bits.lsh`
- [x] `bits.rsh`

### Conversions

- [x] `to_number`

### Units

- [ ] `units.parse`
- [ ] `units.parse_bytes`

### Types

- [x] `is_number`
- [x] `is_string`
- [x] `is_boolean`
- [x] `is_array`
- [x] `is_set`
- [x] `is_object`
- [x] `is_null`
- [x] `type_name`

### Encoding

- [x] `base64.encode`
- [x] `base64.decode`
- [x] `base64url.encode`
- [x] `base64url.encode_no_pad`
- [x] `base64url.decode`
- [x] `urlquery.encode`
- [x] `urlquery.encode_object`
- [x] `urlquery.decode`
- [x] `urlquery.decode_object`
- [x] `json.marshal`
- [x] `json.unmarshal`
- [x] `json.is_valid`
- [x] `yaml.marshal`
- [x] `yaml.unmarshal`
- [x] `yaml.is_valid`
- [x] `hex.encode`
- [x] `hex.decode`

### Token Signing

- [ ] `io.jwt.encode_sign`
- [ ] `io.jwt.encode_sign_raw`

### Token Verification

- [ ] `io.jwt.decode`
- [ ] `io.jwt.decode_verify`
- [ ] `io.jwt.verify_es256`
- [ ] `io.jwt.verify_es384`
- [ ] `io.jwt.verify_es512`
- [ ] `io.jwt.verify_hs256`
- [ ] `io.jwt.verify_hs384`
- [ ] `io.jwt.verify_hs512`
- [ ] `io.jwt.verify_ps256`
- [ ] `io.jwt.verify_ps384`
- [ ] `io.jwt.verify_ps512`
- [ ] `io.jwt.verify_rs256`
- [ ] `io.jwt.verify_rs384`
- [ ] `io.jwt.verify_rs512`

### Time

- [ ] `time.add_date`
- [ ] `time.clock`
- [ ] `time.date`
- [ ] `time.diff`
- [x] `time.now_ns`
- [ ] `time.parse_duration_ns`
- [ ] `time.parse_ns`
- [ ] `time.parse_rfc3339_ns`
- [x] `time.weekday`

### Cryptography

- [x] `crypto.hmac.md5`   
- [x] `crypto.hmac.sha1`
- [x] `crypto.hmac.sha256`
- [x] `crypto.hmac.sha512`
- [x] `crypto.md5`        
- [x] `crypto.sha1`
- [x] `crypto.sha256`
- [ ] `crypto.x509.parse_and_verify_certificates`
- [ ] `crypto.x509.parse_certificate_request`
- [ ] `crypto.x509.parse_certificates`
- [ ] `crypto.x509.parse_rsa_private_key`

### Graphs

- [ ] `graph.reachable`
- [ ] `graph.reachable_paths`
- [ ] `walk`

### GraphQL

- [ ] `graphql.is_valid`
- [ ] `graphql.parse`
- [ ] `graphql.parse_and_verify`
- [ ] `graphql.parse_query`
- [ ] `graphql.parse_schema`

### HTTP

- [ ] `http.send`

### Net

- [ ] `net.cidr_contains`
- [ ] `net.cidr_contains_matches`
- [ ] `net.cidr_expand`
- [ ] `net.cidr_intersects`
- [ ] `net.cidr_merge`
- [ ] `net.cidr_overlap`
- [ ] `net.lookup_ip_addr`

### UUID

- [ ] `uuid.rfc4122`

### Semantic Versions

- [ ] `semver.compare`
- [ ] `semver.is_valid`

### Rego

- [ ] `rego.metadata.chain`
- [ ] `rego.metadata.rule`
- [ ] `rego.parse_module`

### Debugging

Note: `print` calls are erased from plans, so likely can't be supported without support in OPA, or through some hack.

- [ ] `print`

### Tracing

- [ ] `trace`

### OPA

- [x] `opa.runtime`

### Deprecated

- [x] `re_match`
- [x] `cast_array`
- [x] `cast_set`
- [x] `cast_string`
- [x] `cast_boolean`
- [x] `cast_null`
- [x] `cast_object`

## Development

### Testing

* `lein test` to run all tests
* `lein test :unit` to run the Clojure unit tests
* `lein test :compliance` to run the OPA compliance test suite

### Linters

* `lein kibit` to run [kibit](https://github.com/jonase/kibit)
* `lein eastwood` ro run [eastwood](https://github.com/jonase/eastwood)
* `lein clj-kondo --lint src test` to run [clj-kondo](https://github.com/clj-kondo/clj-kondo)

## License

Copyright 2022 Johan Fylling, Anders Eknert

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
