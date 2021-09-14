---
title: Elemento EapType (eaptlsconnectionpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema BaseEapConnectionProperties. Para eaptlsconnectionpropertiesv1schema.
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
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
ms.openlocfilehash: b74341d9b1fdd9121f1d67e2a941d931be049e0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252860"
---
# <a name="eaptype-element-eaptlsconnectionpropertiesv1schema"></a>Elemento EapType (eaptlsconnectionpropertiesv1schema)

El **elemento EapType** es un tipo derivado del elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) del [esquema BaseEapConnectionProperties.](baseeapconnectionpropertiesv1schema-schema.md)

Este elemento **EapType** derivado contiene los siguientes elementos: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation,**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)y [**TLSExtensions.**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)

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
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                                               | Tipo                                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**extendedTLS: PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | Windows 7 y versiones posteriores: indica si se realiza la validación del servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**extendedTLS: AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | Windows 7 y versiones posteriores: indica si se lee el nombre de un servidor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**extendedTLS: TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | Windows 7 y versiones posteriores: permite futuras mejoras en el esquema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | Contiene información sobre la ubicación del certificado de seguridad de nivel de transporte de EAP (EAP-TLS). <br/> El [**elemento CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | boolean                                                                                                           | Determina qué nombre de usuario va a usar EAP-TLS. <br/> Si el [**elemento DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) es **TRUE,** EAP-TLS debe usar un nombre de usuario distinto del nombre que aparece en el certificado. Si el [**elemento DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) es **FALSE,** EAP-TLS usa el nombre de usuario que aparece en el certificado.<br/> El [**elemento DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) es opcional. <br/> |
| [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | Contiene información sobre cómo realizar la validación del servidor. El [**elemento ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) es opcional. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Eaptlsconnectionpropertiesv1 Schema Elements](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





