---
title: TLSExtensionsType Complex Type
description: Obtenga información sobre el tipo complejo TLSExtensionsType. Este tipo permite futuras mejoras en el esquema.
ms.assetid: 5e4f8ef8-1adb-4683-8001-ba7d2d392523
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ac12ad6d3b1229f4fcb75506a9e7ae7655db0287ad58fa9a8079ba12c14e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984114"
---
# <a name="tlsextensionstype-complex-type"></a>TLSExtensionsType Complex Type

El **tipo complejo TLSExtensionsType** permite futuras mejoras en el esquema.


```XML
<xs:complexType name="TLSExtensionsType">
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

El **elemento TLSExtensionsType** es opcional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2 Complex Types](eaptlsconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**TLSExtensions (TLSExtensionsType)**](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 




