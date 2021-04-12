---
title: Tipo complejo de PeapExtensionsType (propiedades de conexión)
description: Obtenga información sobre el tipo complejo de PeapExtensionsType. Este tipo permite futuras mejoras en el esquema.
ms.assetid: d4f7784d-d426-4da6-bf81-40716f185416
keywords:
- Tipo complejo PeapExtensionsType EAPHost
topic_type:
- apiref
api_name:
- PeapExtensionsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bf7e22a013bbd7a931b61b55ae0013bb42f4e41
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359424"
---
# <a name="peapextensionstype-complex-type-connection-properties"></a>Tipo complejo de PeapExtensionsType (propiedades de conexión)

El tipo complejo **PeapExtensionsType** permite futuras mejoras en el esquema.

``` syntax
<xs:complexType name="PeapExtensionsType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Observaciones

El tipo complejo **PeapExtensionsType** es opcional.

## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





