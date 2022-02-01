# Documentation Site
This application deploys a static site to S3. These documents are document all Tu Biomics processes and applications.

# Deployment
Deployments should be handled with github actions, however, if you plan on deploying locally you can run the following,

```
mkdocs build
AWS_PROFILE=myprofile aws s3 sync ./site s3://<my-bucket>
```

# Public Access
Once deployed you can visit the docs online at `http://tubiomics-documentation.s3-website-us-west-1.amazonaws.com/`