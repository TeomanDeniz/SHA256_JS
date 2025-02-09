# SHA256 JavaScript Implementation

## Overview
This JavaScript implementation of the SHA-256 hashing algorithm is originally based on the work of [Chris Veness](https://www.movable-type.co.uk/scripts/sha256.html) and has been adapted and optimized for flexibility.

## Features
- Pure JavaScript implementation (no dependencies required).
- Supports UTF-8 encoding.
- Accepts input in string or hex-byte format.
- Returns the hash in HEX or space-separated HEX format.

## Usage

### Function Signature
```javascript
SHA256(VARIABLE, OPTIONS = {})
```

### Parameters
- `VARIABLE` (string): The input string to be hashed.
- `OPTIONS` (object, optional):
  - `VARIABLE_FORMAT` (string, default: "STRING"): Determines the input format.
    - "STRING" (default) for standard text input.
    - "HEX-BYTES" for hexadecimal byte input.
  - `OUT_FORMAT` (string, default: "HEX"): Determines the output format.
    - "HEX" (default) for standard hexadecimal output.
    - "HEX-W" for space-separated hexadecimal output.

### Example Usage
```javascript
const hash = SHA256("Hello, World!");
console.log(hash); // Output: SHA-256 hash in HEX format

const hashWithOptions = SHA256("Hello, World!", {OUT_FORMAT: "HEX-W"});
console.log(hashWithOptions); // Output: SHA-256 hash in spaced HEX format
```

## Implementation Details
This implementation follows the SHA-256 standard, including:
- UTF-8 encoding support for input strings.
- Padding according to the SHA-256 specification.
- Processing blocks of 512-bit chunks.
- Applying the SHA-256 compression function with bitwise operations.

## License
This implementation is based on Chris Veness's work and follows a permissive open-source approach. So, basically it is MIT Licence.
