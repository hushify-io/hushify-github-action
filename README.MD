# 🔐 Hushify – GitHub Action

Securely fetch a **one-time secret** from [hushify.io](https://www.hushify.io) in your GitHub Actions workflows.

Supports:
- ✔ Full hushify URL
- ✔ Raw hushify token

---

## 🚀 Usage

### Basic example

```yaml
- uses: hushifyio/hushify-github-action@v1
  id: hush
  with:
    hushify: ExampleTokenbrMscBHrE20rnmL0nZ

- run: |
    echo "Using secret"
    ./deploy.sh --token "${{ steps.hush.outputs.secret }}"
