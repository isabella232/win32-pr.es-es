---
title: elemento sidType (ChannelPublishingType)
description: Determina si se debe incluir un identificador de seguridad (SID) de la entidad de seguridad con cada evento escrito en el canal.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- Elemento sidType EventLog
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41653a1fbda3400b74ca5302deb8075ae891e69f22ca0f0e88b6ec4dbb58dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589157"
---
# <a name="sidtype-channelpublishingtype-element"></a>elemento sidType (ChannelPublishingType)

Determina si se debe incluir un identificador de seguridad (SID) de la entidad de seguridad con cada evento escrito en el canal.

``` syntax
<xs:element name="sidType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="None"
             />
            <xs:enumeration
                value="Publishing"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El tipo complejo [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) define el elemento **sidType.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**publicación (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





