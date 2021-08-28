---
title: Elemento AnonymousUserName (IdentityPrivacyParameters)
description: Contiene una identidad anónima usada en lugar de la identificación verdadera de un usuario. Se envía durante la primera fase de la autenticación PEAP cuando identity se envía como texto sin formato.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Elemento AnonymousUserName EAPHost
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
ms.openlocfilehash: cc0a4937eb0a136570d08fcbe18ba69b256ab9b7333d793f6b512dfd87286f8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904032"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a>Elemento AnonymousUserName (IdentityPrivacyParameters)

El **elemento AnonymousUserName (IdentityPrivacyParameters)** contiene una identidad anónima que se usa en lugar de la identificación verdadera de un usuario. Se envía durante la primera fase de la autenticación PEAP cuando **identity** se envía como texto sin formato.

El uso de identidades anónimas viene determinado [**por el elemento EnableIdentityPrivacy.**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md)

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

El **elemento AnonymousUserName** se define mediante [IdentityPrivacyParameters.](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)

## <a name="remarks"></a>Comentarios

El **elemento AnonymousUserName** es opcional.

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

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Mspeapconnectionpropertiesv2 Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





