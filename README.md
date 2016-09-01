# aem-dps
Adobe Experience Manager Endpoints for Adobe On Demand Services

#### Creating a Collection 
curl -u admin:admin -d ":operation=dpsapps:createCollection&dps-title=myTitle&collectionName=myCollection&dps-layout=&template=/libs/mobileapps/dps/templates/collection/default" http://\<server-ip\>:4502/content.html/<path-to-app>

Generates:
```
{
  jcr:primaryType: "cq:PageContent",
  jcr:createdBy: "admin",
  jcr:title: "myTitle",
  cq:template: "/libs/mobileapps/dps/templates/collection/default",
  dps-resourceType: "dps:Collection",
  jcr:created: "Thu Sep 01 2016 14:55:40 GMT-0400",
  cq:lastModified: "Thu Sep 01 2016 14:55:40 GMT-0400",
  sling:resourceType: "mobileapps/dps/components/page/collection/collection",
  cq:lastModifiedBy: "admin",
  dps-title: "myCollection"
}
```

#### Uploading a Collection from AEM to Adobe On Demand Services
curl -u admin:admin -d ":operation=dpsapps:dpsUpload&createIfMissing=true&includeContent=true" http://\<server-ip\>:4502/content/mobileapps/\<app\>/collections/myCollection

