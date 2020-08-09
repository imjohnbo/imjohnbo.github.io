---
layout: post
title: "Google Cloud Storage Introduction"
author: john
categories: [ Technology ]
tags: [ GitHub, GitHub Actions, Google Cloud ]
comments: false
image: assets/images/2020-08-09-google-cloud.jpg
---

[Google Cloud Storage](https://cloud.google.com/storage) is a "RESTful online file storage web service for storing and accessing data on Google Cloud Platform infrastructure" [[Wikipedia](https://en.wikipedia.org/wiki/Google_Storage)], comparable to [Amazon S3](https://aws.amazon.com/s3/) or [Azure Blob Storage](https://azure.microsoft.com/en-us/services/storage/blobs/). Let's figure out how to use it!

_Originally presented at my local programmer's gathering – slides are available [here](https://docs.google.com/presentation/d/e/2PACX-1vSQ-M68oMLMabk6m22uTaCr72W066tJ9pC5MOdTMV-UCWCbVQrOJGyRDWviyLZBR7q1cYvgcxXT8upr/pub?start=false&loop=false&delayms=3000&slide=id.p) and GitHub repository at [https://github.com/imjohnbo/gcs-demo](https://github.com/imjohnbo/gcs-demo)._

## Goals

Although I had used other products in the Google Cloud Platform (GCP) ecosystem, I hadn't ever tried to host a static website from Cloud Storage. Its [low cost](https://cloud.google.com/storage/pricing) and low barrier of entry make it an easy dip into GCP.

After an intial manual upload, I hooked up GitHub Actions automation to it to continuously deploy changes to a certain file. My go-to static website has become [octocat](https://github.com/imjohnbo/octocat), taken from [https://api.github.com/octocat](https://api.github.com/octocat), so that's what I used here.

![octocat screenshot](/assets/images/2020-08-09-octocat.jpg)

## Method and automation

_Full setup steps are listed [here](https://github.com/imjohnbo/gcs-demo#steps) and automation [here](https://github.com/imjohnbo/gcs-demo#automatic-deploys-using-github-actions-optional), and following is a summary._

Before beginning, you'll need a Google Cloud Platform account and to install the `gcloud` CLI. New customers get $300 of [free  credit](https://cloud.google.com/free) to use on the paid features of GCP like GCS.

Log into the CLI and create a new project, linking it to your billing account (with or without the $300 credit 🤑). As always, it's important to create an app-specific, rights-restricted service account. In this case, give it the Storage Admin role. Now you can use the `gsutil` CLI (should also be installed with `gcloud`) to create a bucket and upload your `index.html` file to it. It's that easy! 😍 Because this is a public website, open it up to the public internet and navigate to it at a website like [https://storage.googleapis.com/your-bucket-name/index.html](https://storage.googleapis.com/your-bucket-name/index.html). Then hook it up to HTTP(S) Load Balancing and a custom domain as in this "[Hosting a static website](https://cloud.google.com/storage/docs/hosting-static-website)" tutorial.

And finally, try out a GitHub Actions workflow like [this](https://github.com/imjohnbo/gcs-demo/blob/main/.github/workflows/upload.yml) that uploads `index.html` to GCS after every change!

About pricing: I take it from [the GCP pricing calculator](https://cloud.google.com/products/calculator) that hitting a 50 MB web page (!!!!) located in Iowa 50,000 times / month would cost under a dollar.

![octocat screenshot](/assets/images/2020-08-09-pricing.jpg)

---

Happy GCS-ing!

--John