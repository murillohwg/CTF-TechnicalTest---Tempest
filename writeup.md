# Valdoria CTF Writeup

## Recon

Initial exploration of the platform.

## OSINT

Discovery of confidential files.

## Hash Analysis

A custom Python script was used to brute-force date-based hashes.

## JWT Authentication Bypass

The application failed to properly validate the JWT signature.

Header:

{
 "alg":"none",
 "typ":"JWT"
}

Payload:

{
 "name":"Tavares Lunik Bernardi",
 "role":"operador"
 "Authorization:""Bearer TOKEN_FORMATO_JWT"
}

## Exploitation

Using curl, a crafted JWT was sent to the admin endpoint.

## Impact

Access to restricted administrative data.