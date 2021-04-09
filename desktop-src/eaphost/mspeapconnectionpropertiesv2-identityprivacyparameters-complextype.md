---
title: Tipo complejo de IdentityPrivacyParameters
description: Contiene información sobre el uso de identidad anónima durante la autenticación PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104149021"
---
# <a name="identityprivacyparameters-complex-type"></a>Tipo complejo de IdentityPrivacyParameters

El tipo complejo **IdentityPrivacyParameters** contiene información sobre el uso de identidad anónima durante la autenticación PEAP.


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| Elemento                                                                                                               | Tipo    | Descripción                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | boolean | Indica si se envía la verdadera identidad de un usuario o una identidad anónima.                                                                                                                                                                                                                                                                           |
| [**AnonymousUserName**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | string  | contiene una identidad anónima que se utiliza en lugar de la verdadera identificación de un usuario. Se envía durante la primera fase de la autenticación PEAP cuando la **identidad** se envía como texto sin formato. El uso de identidades anónimas viene determinado por el elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) . |



 

## <a name="remarks"></a>Observaciones

El elemento IdentityPrivacyParameters es opcional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Tipos complejos de mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




