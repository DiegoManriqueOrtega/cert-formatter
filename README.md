# cert-formatter

Browser tool for formatting certificates and private keys from Outgoing Integration configs.

Paste a JSON payload or raw escaped string. Extracts any PEM block, strips `\n` escape sequences, re-wraps the base64 body at 64 chars per line, and copies the result to clipboard automatically.

## Input formats

**JSON with escaped string (typical Outgoing Integration payload)**

```json
{
  "privateKey": "-----BEGIN PRIVATE KEY-----\nMIIEvQIBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQC7o4qne60TB3wp\nGp8UPFqRGQqEA3NNm9V4sEMI6oHl0y6RKSmadVPpJqILMpHiLTidE2xNgYEJ\n-----END PRIVATE KEY-----"
}
```

**Output**

```
-----BEGIN PRIVATE KEY-----
MIIEvQIBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQC7o4qne60TB3wp
Gp8UPFqRGQqEA3NNm9V4sEMI6oHl0y6RKSmadVPpJqILMpHiLTidE2xNgYEJ
-----END PRIVATE KEY-----
```

Also accepts raw PEM and escaped strings without a JSON wrapper. Works with certificates, private keys, and certificate chains (multiple PEM blocks).

## Usage

Go to the github pages site and use it: https://diegomanriqueortega.github.io/cert-formatter/
