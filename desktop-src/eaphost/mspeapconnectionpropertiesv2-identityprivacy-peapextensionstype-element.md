---
title: Elemento IdentityPrivacy (PeapExtensionsType)
description: El elemento IdentityPrivacy (PeapExtensionsType) indica si la identidad verdadera de un usuario se envía en el esquema mspeapconnectionpropertiesv2.
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- Elemento IdentityPrivacy EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0a23ce28a1a807bb948c114435463102561570b
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988951"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a>Elemento IdentityPrivacy (PeapExtensionsType)

El **elemento IdentityPrivacy (PeapExtensionsType)** indica si se envía la identidad verdadera de un usuario o una identidad anónima.

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

El **elemento IdentityPrivacy** se define mediante el [**elemento PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)

## <a name="remarks"></a>Comentarios

El **elemento IdentityPrivacy** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Mspeapconnectionpropertiesv2 Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





