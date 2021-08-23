---
title: Tipo complejo IdentityPrivacyParameters
description: Contiene información sobre el uso de identidades anónimas durante la autenticación PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 18bef3eb69ab2799f7139fe2886d89e996fb8fb47d178997694c568450fb8340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983905"
---
# <a name="identityprivacyparameters-complex-type"></a>Tipo complejo IdentityPrivacyParameters

El **tipo complejo IdentityPrivacyParameters** contiene información sobre el uso de identidades anónimas durante la autenticación peap.


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
| [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | boolean | Indica si se envía la identidad verdadera de un usuario o una identidad anónima.                                                                                                                                                                                                                                                                           |
| [**AnonymousUserName**](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | string  | contiene una identidad anónima usada en lugar de la identificación verdadera de un usuario. Se envía durante la primera fase de la autenticación PEAP cuando **identity** se envía como texto sin formato. El uso de identidades anónimas viene determinado [**por el elemento EnableIdentityPrivacy.**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) |



 

## <a name="remarks"></a>Comentarios

El elemento IdentityPrivacyParameters es opcional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Mspeapconnectionpropertiesv2 Schema](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Mspeapconnectionpropertiesv2 Complex Types](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




