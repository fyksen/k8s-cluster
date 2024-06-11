# Sops secrets

I followed [this](https://fluxcd.io/flux/guides/mozilla-sops/) guide.

```
export KEY_NAME="k8s-rlnc"
export KEY_COMMENT="flux secrets"

gpg --batch --full-generate-key <<EOF
%no-protection
Key-Type: 1
Key-Length: 4096
Subkey-Type: 1
Subkey-Length: 4096
Expire-Date: 0
Name-Comment: ${KEY_COMMENT}
Name-Real: ${KEY_NAME}
EOF
```