---
title: Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)
description: Indica si se envía la identidad verdadera de un usuario o una identidad anónima. | Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- Elemento EnableIdentityPrivacy EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3501bbfa09222f862dc5b53c610922cf43c0d7e68657bfc528ede49a74249ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117903954"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a>Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)

El **elemento EnableIdentityPrivacy (IdentityPrivacyParameters)** indica si se envía la identidad verdadera de un usuario o una identidad anónima.

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

[IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) define el elemento **EnableIdentityPrivacy** .

## <a name="remarks"></a>Comentarios

El **elemento EnableIdentityPrivacy** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





