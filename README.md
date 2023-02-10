# Serverleta

This GitHub Action compares the current serverless state with the latest version in an S3 bucket, and posts the difference as a comment on the pull request.
Usage

Create a workflow that uses this action:
```
    - name: Serverleta Plan
      uses: actions/serverleta@latest
      with:
        s3: "s3-bucvket-name"
        build: "make build-command"
      env:
         AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
         AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
```
