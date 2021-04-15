---
title: Elemento AnonymousUserName (IdentityPrivacyParameters)
description: Contiene una identidad anónima que se utiliza en lugar de la verdadera identificación de un usuario. Se envía durante la primera fase de la autenticación PEAP cuando la identidad se envía como texto sin formato.
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
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422456"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a>Elemento AnonymousUserName (IdentityPrivacyParameters)

El elemento **AnonymousUserName (IdentityPrivacyParameters)** contiene una identidad anónima que se utiliza en lugar de la verdadera identificación de un usuario. Se envía durante la primera fase de la autenticación PEAP cuando la **identidad** se envía como texto sin formato.

El uso de identidades anónimas viene determinado por el elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

El elemento **AnonymousUserName** se define mediante [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .

## <a name="remarks"></a>Observaciones

El elemento **AnonymousUserName** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



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

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





