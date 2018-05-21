---
swagger: "2.0"
x-collection-name: Azure DevTest Labs
x-complete: 1
info:
  title: DevTestLabsClient
  description: the-devtest-labs-client
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/labs/{labName}/notificationchannels
  : get:
      summary: Notification Channels List
      description: List notificationchannels in a given lab.
      operationId: NotificationChannels_List
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftdevtestlablabslabnamenotificationchannels-get
      parameters:
      - in: query
        name: $expand
        description: Specify the $expand query
      - in: query
        name: $filter
        description: The filter to apply to the operation
      - in: query
        name: $orderby
        description: The ordering expression for the results, using OData notation
      - in: query
        name: $top
        description: The maximum number of resources to return from the operation
      - in: path
        name: labName
        description: The name of the lab
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Notification Channels
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/labs/{labName}/notificationchannels/{name}
  : get:
      summary: Notification Channels Get
      description: Get notificationchannel.
      operationId: NotificationChannels_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftdevtestlablabslabnamenotificationchannelsname-get
      parameters:
      - in: query
        name: $expand
        description: Specify the $expand query
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the notificationChannel
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Notification Channels
    put:
      summary: Notification Channels Create Or Update
      description: Create or replace an existing notificationChannel.
      operationId: NotificationChannels_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftdevtestlablabslabnamenotificationchannelsname-put
      parameters:
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the notificationChannel
      - in: query
        name: No Name
      - in: body
        name: notificationChannel
        description: A notification
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Notification Channels
    delete:
      summary: Notification Channels Delete
      description: Delete notificationchannel.
      operationId: NotificationChannels_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftdevtestlablabslabnamenotificationchannelsname-delete
      parameters:
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the notificationChannel
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Notification Channels
    patch:
      summary: Notification Channels Update
      description: Modify properties of notificationchannels.
      operationId: NotificationChannels_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftdevtestlablabslabnamenotificationchannelsname-patch
      parameters:
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the notificationChannel
      - in: query
        name: No Name
      - in: body
        name: notificationChannel
        description: A notification
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Notification Channels
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.DevTestLab/labs/{labName}/notificationchannels/{name}/notify
  : post:
      summary: Notification Channels Notify
      description: Send notification to provided channel.
      operationId: NotificationChannels_Notify
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftdevtestlablabslabnamenotificationchannelsnamenotify-post
      parameters:
      - in: path
        name: labName
        description: The name of the lab
      - in: path
        name: name
        description: The name of the notificationChannel
      - in: query
        name: No Name
      - in: body
        name: notifyParameters
        description: Properties for generating a Notification
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Notification Channels
---