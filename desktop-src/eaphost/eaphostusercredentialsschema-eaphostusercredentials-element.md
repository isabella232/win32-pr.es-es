---
title: Elemento EapHostUserCredentials
description: Contiene el elemento EapMethod y el elemento Credentials o CredentialsBlob.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- EapHostUserCredentials, elemento EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a18922ef19bd828067ddb0153aa7c6369ecfeebd0446f5a6481f91fa64ca21b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274425"
---
# <a name="eaphostusercredentials-element"></a>Elemento EapHostUserCredentials

El **elemento EapHostUserCredentials** contiene el [**elemento EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) y [**el elemento Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) [**o CredentialsBlob.**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md)

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                | Tipo                                                                                                                | Descripción                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Credenciales**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [**BaseEapMethodUserCredentials**](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | Se usa cuando la configuración del método está en formato de texto XML en lugar de un blob binario.<br/>   |
| [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | hexBinary                                                                                                           | Se usa cuando la configuración del método es un BLOB binario en lugar de en formato de texto XML.<br/> |
| [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                                                  | Identifica el método al que se hace referencia. <br/>                                             |



## <a name="remarks"></a>Comentarios

Los [**elementos Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) y [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) no se pueden usar simultáneamente.

Hay un punto de extensión para otros espacios de nombres.

El **elemento processContents** permite futuras mejoras en el esquema. El **elemento processContents** es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





