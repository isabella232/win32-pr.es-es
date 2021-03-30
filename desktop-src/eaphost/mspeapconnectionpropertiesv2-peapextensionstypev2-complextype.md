---
title: Tipo complejo de PeapExtensionsTypeV2
description: Obtenga información sobre el tipo complejo de PeapExtensionsTypeV2. Este tipo permite futuras mejoras en el esquema.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869e67f16bc9b42929d227755e08bf6924dcc737
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995642"
---
# <a name="peapextensionstypev2-complex-type"></a>Tipo complejo de PeapExtensionsTypeV2

El tipo complejo **PeapExtensionsTypeV2** permite futuras mejoras en el esquema.


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



## <a name="remarks"></a>Observaciones

El elemento **PeapExtensionsTypeV2** es opcional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Tipos complejos de mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




