# Serverleta

This GitHub Action compares the current serverless state with the latest version in an S3 bucket, and posts the difference as a comment on the pull request.
Usage

Create a workflow that uses this action:
```yaml
    - name: serverleta
      uses: loadfms/serverleta@v1.0.7
      with:
        s3: "s3-bucket-name"
        build: "make build-command"
        aws_access_key_id: ${{ secrets.AWS_ACCESS_KEY_ID }}
        aws_secret_access_key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
        github_token: ${{ secrets.TOKEN }}
```
