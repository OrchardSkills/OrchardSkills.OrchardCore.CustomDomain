# Adding A Secure Custom Domain to an Azure App Service

## [YouTube Video](https://youtu.be/0Tadyu5yqU0)

[![OrchardSkillsYouTubeThumbNailSSL](https://user-images.githubusercontent.com/59172485/90436229-85525f00-e08d-11ea-98ad-b797ebc5e557.png)](https://youtu.be/0Tadyu5yqU0)

# Introduction

In this article we are going to setup a custom domain with SSL certificates  with let's encrypt.

![Custom-Domain-Azure-001](https://user-images.githubusercontent.com/59172485/90436151-710e6200-e08d-11ea-9320-f083eafaa349.png)

Login to your Azure portal and go to your App Service.

![Custom-Domain-Azure-002](https://user-images.githubusercontent.com/59172485/90436153-71a6f880-e08d-11ea-9721-63bba24347bb.png)

Select the Custom domain on the side menu. Select "On" in the HTTPS only settings.

![Custom-Domain-Azure-003](https://user-images.githubusercontent.com/59172485/90436154-723f8f00-e08d-11ea-8777-dafd935ebffc.png)

Click on the "Add custom domain" link.

![Custom-Domain-Azure-004](https://user-images.githubusercontent.com/59172485/90436155-72d82580-e08d-11ea-8cc7-52e633039f96.png)

Enter your custom domain and press the "Validate" button.

![Custom-Domain-Azure-005](https://user-images.githubusercontent.com/59172485/90436157-7370bc00-e08d-11ea-89bb-de0f681fa51e.png)

Switch over to your hosting provider and edit the A records and enter in the specified IP address.

![Custom-Domain-Azure-006](https://user-images.githubusercontent.com/59172485/90436159-7370bc00-e08d-11ea-8881-fd2589a817d0.png)

Add a "TXT" record with your-domain.azurewebsite.net.

![Custom-Domain-Azure-007](https://user-images.githubusercontent.com/59172485/90436160-74095280-e08d-11ea-9492-ff3af4800b83.png)

Press the "Validate" button again to verify you have ownership of the domain.

![Custom-Domain-Azure-008](https://user-images.githubusercontent.com/59172485/90436162-74a1e900-e08d-11ea-9fd4-83d32a3adaf9.png)

With your favorite browser browse to the website https://www.sslforfree.com/.

![Custom-Domain-Azure-009](https://user-images.githubusercontent.com/59172485/90436165-753a7f80-e08d-11ea-9545-2e0472af0b01.png)

Select Manual Verification (DNS) and press the "Manual Verification" button.

![Custom-Domain-Azure-010](https://user-images.githubusercontent.com/59172485/90436168-75d31600-e08d-11ea-9246-60531c03f463.png)

Enter the TXT Records for the web site specified by SSL For Free

![Custom-Domain-Azure-011](https://user-images.githubusercontent.com/59172485/90436170-75d31600-e08d-11ea-8baa-5e5b0cbb026b.png)

Enter the TXT records for the www prefix for the web site specified by SSL For Free.

![Custom-Domain-Azure-012](https://user-images.githubusercontent.com/59172485/90436173-766bac80-e08d-11ea-9f69-b73c4754f38f.png)

After the verification successful, press the "Download SSL Certificates" button.

![Custom-Domain-Azure-013](https://user-images.githubusercontent.com/59172485/90436176-77044300-e08d-11ea-8ea1-e218518dbb5f.png)

Either cut and paste the specified information or better yet download retrieve the information from the downloaded files.

![Custom-Domain-Azure-014](https://user-images.githubusercontent.com/59172485/90436188-78ce0680-e08d-11ea-9407-0f1a95b32566.png)

Convert the SSL Certificates to PFX Certificate (PKCS#12) format.

![Custom-Domain-Azure-015](https://user-images.githubusercontent.com/59172485/90436192-79669d00-e08d-11ea-8ae5-331ae59b3983.png)

Press the "Add custom domain" link. Enter the Custom domain and then press the "Add custom domain" button.

![Custom-Domain-Azure-016](https://user-images.githubusercontent.com/59172485/90436201-7bc8f700-e08d-11ea-869b-39184c08c1c7.png)

Select you custom domain from the combo box pull down. and then press the "Upload PFX Certificate".

![Custom-Domain-Azure-017](https://user-images.githubusercontent.com/59172485/90436204-7e2b5100-e08d-11ea-92fa-49968ffb62a3.png)

Enter the certificate password and press the "Upload" button.

![Custom-Domain-Azure-018](https://user-images.githubusercontent.com/59172485/90436210-808dab00-e08d-11ea-8d6a-ab5661a7e34a.png)

Select "SNI SSL" from the "TLS/SSL Type" and press the "Add Binding" button.

![Custom-Domain-Azure-019](https://user-images.githubusercontent.com/59172485/90436218-81bed800-e08d-11ea-9829-2297b17b5acc.png)

With your favorite browser, browse to your custom domain.

![Custom-Domain-Azure-020](https://user-images.githubusercontent.com/59172485/90436220-82576e80-e08d-11ea-9a64-ff8d65375e46.png)

Click on the Add custom domain and  Validate button. Notice you need to verify domain ownership.

![Custom-Domain-Azure-021](https://user-images.githubusercontent.com/59172485/90436221-82f00500-e08d-11ea-842e-2d20123a19f3.png)

Enter a "CNAME" for the azure website.

![Custom-Domain-Azure-022](https://user-images.githubusercontent.com/59172485/90436223-83889b80-e08d-11ea-8465-989c7c447fdc.png)

if desired, add another custom domain for the www prefix. Click on the Add custom domain with the www prefix and press validate.  

![Custom-Domain-Azure-023](https://user-images.githubusercontent.com/59172485/90436224-84213200-e08d-11ea-8866-7cb1b19de812.png)

Select custom domain,  "SNI SSL" from the "TLS/SSL Type" and press the "Add Binding" button.

![Custom-Domain-Azure-024](https://user-images.githubusercontent.com/59172485/90436225-84b9c880-e08d-11ea-910d-09fa8e97a306.png)

Now both domains are secure with SSL Certificates.

![Custom-Domain-Azure-025](https://user-images.githubusercontent.com/59172485/90436227-84b9c880-e08d-11ea-8233-eb6d309a0fbc.png)



With your favorite browser, browse to your site and test.

# Conclusion

With the free certificates from Let's Encrypt you can have a secure site.



# GitHub

The complete source code is located [here](https://github.com/OrchardSkills/OrchardSkills.OrchardCore.CustomDomain).