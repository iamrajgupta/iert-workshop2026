# Task 01 – FlowVault Security Findings

## Security Assessment

| Rank | Vulnerability | Severity |
|---|---|---|
| 1 | Admin privilege escalation through role cookie | Critical |
| 2 | IDOR in order details API | Critical |
| 3 | SSRF in URL importer | Critical |
| 4 | Mass assignment in profile API | Critical |
| 5 | Unprotected admin users API | High |
| 6 | Plaintext password storage | High |
| 7 | Session token weaknesses and leakage | High |
| 8 | Unrestricted file upload | High |
| 9 | Coupon race condition and duplicate redemption | High |
| 10 | Stored XSS risk in comments | High |

## Additional Findings

- Sensitive profile data exposure.
- Missing session expiry.
- Permissive CORS configuration.
- Missing input validation.
- Sensitive authentication tokens printed in server logs.
- File upload size restrictions are missing.

## Evidence Reviewed

- `src/middleware.ts`
- `src/lib/db.ts`
- `src/app/api/auth/login/route.ts`
- `src/app/api/profile/route.ts`
- `src/app/api/admin/users/route.ts`
- `src/app/api/import-url/route.ts`
- `src/app/api/upload/route.ts`
- `src/app/api/coupons/redeem/route.ts`
- `src/app/api/orders/[id]/route.ts`
- `src/app/api/comments/route.ts`

## Status

Initial security assessment completed. Findings require further validation and remediation.
