---
title: Elemento EapType (mspeapconnectionpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema BaseEapConnectionProperties. Para mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
keywords:
- EapType, elemento EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 47f3585f35b2e7ee7722cdd99c90605cdb7864b2211fcf28f7ec0ac662b5289b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719779"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a>Elemento EapType (mspeapconnectionpropertiesv1schema)

El **elemento EapType** es un tipo derivado del [**elemento EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) del [esquema BaseEapConnectionProperties.](baseeapconnectionpropertiesv1schema-schema.md)

Este elemento **EapType** derivado contiene los siguientes elementos: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks,**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) y [**PeapExtensions.**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                     | Tipo                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | Describe el método interno y la configuración del método. Si el [**elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) es TRUE, el [**elemento Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) debe estar presente. Si el [**elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) es FALSE, el [**elemento Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) debe estar ausente.<br/>           |
| [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | boolean                                                                                                         | Indica si se deben realizar comprobaciones de protección de acceso a redes (NAP). Si el [**elemento EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) es TRUE, PEAP realizará comprobaciones nap; si FALSE PEAP no realizará comprobaciones nap. El [**elemento EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) es opcional.<br/>                                                                                |
| [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | boolean                                                                                                         | Indica si se debe realizar una reconexión rápida. Si el [**elemento FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) es TRUE, PEAP intenta realizar una reconexión rápida. si es FALSE, PEAP realiza la autenticación completa. El [**elemento FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) es opcional.<br/>                                                                                                                       |
| [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [**IdentityPrivacyParameters**](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | Windows 7 o posterior: indica si se envía la identidad verdadera de un usuario o una identidad anónima. El [**elemento IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) es opcional.<br/>                                                                                                                                                                                                                                                                                 |
| [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | boolean                                                                                                         | Indica si se debe realizar el acceso GUEST. Si el [**elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) es TRUE, el [**elemento Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) debe estar presente y describir el método interno y su configuración; si es FALSE, PEAP realizará el acceso GUEST. El [**elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) es opcional.<br/>            |
| [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | El [**elemento PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) permite futuras mejoras en el esquema. El [**elemento PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) es opcional.<br/>                                                                                                                                                                                                                                    |
| [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | boolean                                                                                                         | Indica si se debe autenticar con servidores que admiten el enlace criptográfico. Si el [**elemento RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) es TRUE, PEAP se autenticará con servidores que no admiten cryptobinding; si es FALSE, PEAP solo se autenticará con servidores que admitan el enlace criptográfico. El [**elemento RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) es opcional.<br/> |
| [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | Contiene información sobre cómo realizar la validación del servidor. El [**elemento ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) es opcional.<br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





