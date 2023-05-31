---
share: true
---
# website
## jamstack
* [jamstack.org](https://jamstack.org/)  
  💡the idea is a static (precompiled) page for maximum performance
  * [netlify](https://www.netlify.com/)
  * [aws amplify](https://aws.amazon.com/de/amplify/)
  * [cloudflare pages](https://pages.cloudflare.com/)
  * [bejamas.io](https://bejamas.io/services/jamstack-website/)
  good overview with even more service
### static site generators
* [hugo](https://gohugo.io/)
* [jekyll](https://jekyllrb.com/)
	* [jekyll themes](https://jekyllthemes.io/free)
* [gatsby](https://www.gatsbyjs.com/)
### static site hosting
* netlify
* vercel
* cloudflare pages
* aws (amplify, cloudstack, lightsail, S3)
* firebase (google cloud platform)
* [render](https://render.com/pricing)
## traditional
* [django](https://www.djangoproject.com/) (python backend)
integrated ORM
* [angular](https://angular.io/) (frontend framework)
* [express](https://expressjs.com/de/) (Node.js frontend framework)
## misc
* [netlify](https://www.netlify.com/)
ecosystem to build high performance sites & apps
e.g. build and deploy static website from github repository
* [ghost](https://ghost.org/)
publish, share a business around content
easy, extensive CMS with integrations and API can be used with other frontends (hugo, next.js, gatsby ...)
easily integrates subscriptions and payment
## use cases
### hosting static website with oauth2 iam
Using AWS (Cognito/Cloudfront/S3/Lambda@Edge)
auth flow is an issue, can't happen in cloudfront (auth header could be cached) therefore lambda necessary
* tried out #[authorization @ edge](https://aws.amazon.com/de/blogs/networking-and-content-delivery/authorizationedge-how-to-use-lambdaedge-and-json-web-tokens-to-enhance-web-application-security/) pitfall jwt is delivered in url (auth not persistant)
* [stackoverflow](https://stackoverflow.com/questions/67031155/aws-static-website-cloudfront-signed-cookies) answer is based on [aws seting signed cookies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-setting-signed-cookie-custom-policy.html)
[AWS Authorization@Edge using cookies](https://aws.amazon.com/de/blogs/networking-and-content-delivery/authorizationedge-using-cookies-protect-your-amazon-cloudfront-content-from-being-downloaded-by-unauthenticated-users/)
[Deploy from AWS Repository](https://console.aws.amazon.com/lambda/home?region=us-east-1#/create/app?applicationId=arn:aws:serverlessrepo:us-east-1:520945424137:applications/cloudfront-authorization-at-edge)
## conclusion
There is no one fits all approach.
For (small) static sites a statically generated page seems the best way to go, preferably "serverless".
If the Page shall have additional functionallity static might not be the way to go.
## pictures

|from [bejamas.io](bejamas.io)|
|---|
|![[../jamstack.png|jamstack.png]]|