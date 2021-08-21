---
title: PeapExtensionsTypeV2 Complex Type
description: Obtenga información sobre el tipo complejo PeapExtensionsTypeV2. Este tipo permite futuras mejoras en el esquema.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baea42ec60fe84085ea5e4541848fd43b786419bedab17e938044ff0a713fa07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086034"
---
# <a name="peapextensionstypev2-complex-type"></a>PeapExtensionsTypeV2 Complex Type

El **tipo complejo PeapExtensionsTypeV2** permite futuras mejoras en el esquema.


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a>Comentarios

El **elemento PeapExtensionsTypeV2** es opcional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Mspeapconnectionpropertiesv2 Tipos complejos](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




