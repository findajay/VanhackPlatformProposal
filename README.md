# Vanhack Platform Server less architecture Proposal
<img src="https://dachou.github.io/assets/20181015-event-driven-arch.png"/>

Whether you're a developer or an operations engineer, it’s a good idea to start wrapping your brain around the fundamental concepts of serverless computing. The technology is still in its infancy, but I believe it will radically shift how many applications are built in the years to come.

## What
In this document I am proposing to covert Vanhack web app hosted on azure to serverless computing using storage account.

## How
1. We need to build a handful of Azure resources to support both the front-end and the back-end of the application. We’ll create an Azure Storage account, build an Azure Function.
2. We need to enable static website hosting on storage account.
3. To make your static website files available over your custom domain and HTTPS, we can use Azure CDN to access blobs with custom domains over HTTPS. As a part of this process, we need to point your CDN to the primary static website endpoint as opposed to the primary blob service endpoint. 

## Why

There are many reasons to switch to serverless computing 
1. First is obviously the cost effectiveness. Checkout storage account pricing https://azure.microsoft.com/en-us/pricing/details/storage/blobs/
2. Easy To Deploy
3. Better Scalability
4. Maximum Availability (Using CDN active/passive architecture)
5. Happier Customers
6. Easy multi-tenant management




