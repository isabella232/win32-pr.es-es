---
title: Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)
description: Indica si se envía la verdadera identidad de un usuario o una identidad anónima. | Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)
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
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362353"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a>Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)

El elemento **EnableIdentityPrivacy (IdentityPrivacyParameters)** indica si se envía la verdadera identidad de un usuario o una identidad anónima.

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

El elemento **EnableIdentityPrivacy** se define mediante [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .

## <a name="remarks"></a>Observaciones

El elemento **EnableIdentityPrivacy** es opcional.

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


</dt> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





