---
title: Elemento SID (ChannelPublishingType)
description: Determina si se debe incluir un identificador de seguridad (SID) de la entidad de seguridad con cada evento escrito en el canal.
ms.assetid: 3ce176a3-9e21-4646-8c99-7beb687e6847
keywords:
- elemento SID EventLog
topic_type:
- apiref
api_name:
- sidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d65e1ade4ded95b070b45de9462f6aee2c60ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695958"
---
# <a name="sidtype-channelpublishingtype-element"></a>Elemento SID (ChannelPublishingType)

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

El elemento **SID** se define mediante el tipo complejo de [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Elemento primario**
</dt> <dt>

[**publicación (ChannelType)**](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





