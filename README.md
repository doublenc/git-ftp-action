# git-ftp-action

Uses [git-ftp](https://github.com/git-ftp/git-ftp) and [GitHub actions](https://github.com/features/actions) to deploy a GitHub repository to a FTP server.

## Example usage

```
name: Deploy via git-ftp
on: push
jobs:
  deploy:
    name: Deploy
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: git-ftp push
      uses: sebastianpopp/git-ftp-action@releases/v2
      with:
        url: "ftp://ftp.example.com/path/"
        user: ${{ secrets.FTP_USER }}
        password: ${{ secrets.FTP_PWD }}
```

## Input parameters

Input parameter | Description  | Required
---             | ---          | ---
url             | FTP_DOMAIN   | Yes
user            | FTP_USERNAME | Yes
password        | FTP_PASSWORD | Yes