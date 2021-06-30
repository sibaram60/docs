## Documentation /register
* [/api/v1/register/verify-mobile](#verify-mobile)
* [/api/v1/register/confirm-otp](#confirm-otp)
* [/api/v1/register/resend-otp](#resend-otp)
* [/api/v1/register/register](#register)
 
 This API will guide, to register a user into the site.

## confirm-mobile
[ METHOD - POST ]
this will be the first call from register UI page to the server, to get the OTP.
Field | Type | Constraint
------|------------|------------------
mobile | string | unique and 10 digits of number
password| string | alphanumeric and should more than 6 characters
confirmPassword| string | match the above password field

For example
URL :  http://< base-domain >/v0/api/register/confirm-mobile \
 \
method: POST \
 \
payload is

```javascript
{
  "mobile" : "7894561230",
  "password" : "password",
  "confirmPassword" : "password",
}
```

## confirm-otp
[ METHOD - POST ]
this will be for the validation.

Field | Type | Constraint
------|------------|------------------
mobile | string | unique and 10 digits of number
otp| string | 6 digits


For example
URL :  http://< base-domain >/v0/api/register/confirm-otp \
 \
method: POST \
 \
payload is

```javascript
{
  "mobile" : "7894561230",
  "otp" : "123456",
}
```
## resend-otp
[ METHOD - GET ]
to get anther OTP.

Field | Type | Constraint
------|------------|------------------
mobile | string | unique and 10 digits of number


For example
URL :  http://< base-domain >/v0/api/register/resend-otp/:mobile \
 \
method: GET \
 \
payload will in URL - v0/api/register/resend-otp/:mobile 
