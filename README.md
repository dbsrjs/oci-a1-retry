# oci-a1-retry

Oracle Cloud Always Free ARM(A1) 인스턴스가 「Out of capacity」로 만들어지지 않을 때,
GitHub Actions 가 10분마다 생성을 다시 요청한다. 성공하면 이슈를 열어 알리고 스스로 꺼진다.

설정 값은 `.github/workflows/retry.yml` 의 `env`, 인증은 저장소 Secrets 네 개
(`OCI_USER_OCID` · `OCI_TENANCY_OCID` · `OCI_FINGERPRINT` · `OCI_PRIVATE_KEY`).

인스턴스가 생기면 이 저장소와 Oracle API 키를 지운다.
