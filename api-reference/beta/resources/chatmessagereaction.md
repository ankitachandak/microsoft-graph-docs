---
title: "chatMessageReaction resource type"
description: "Represents a reaction to a chatMessage entity. "
localization_priority: Normal
author: "RamjotSingh"
ms.prod: "microsoft-teams"
doc_type: "resourcePageType"
---

# chatMessageReaction resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a reaction to a [chatMessage](chatmessage.md) entity. 

An entity of type `chatMessageReaction` is returned as part of the [Get channel message](../api/channel-get-message.md) API, as a part of the [chatMessage](chatmessage.md) entity.

## Properties

| Property     | Type        | Description |
|:-------------|:------------|:------------|
|createdDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|reactionType|String|Planned values include: <br><ul><li>Like - Like a message, content is blank in this case.</li><li>Emoji - Emoji reaction. Content is set to unicode value of the emoji.</li><li>Label - Content is set to the string in the label.</li></ul>|
|user|[identitySet](identityset.md)|The user who reacted to the message.|

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chatMessageReaction",
  "baseType": null
}-->

```json
{
  "createdDateTime": "String (timestamp)",
  "reactionType": "String",
  "user": {"@odata.type": "microsoft.graph.identitySet"}
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chatMessageReaction resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
