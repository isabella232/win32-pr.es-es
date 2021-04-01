---
title: Tipo complejo de CredentialsSourceParameters
description: Define el elemento necesario para especificar el origen del certificado que se va a utilizar con una autenticación EAP-TLS.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- Tipo complejo CredentialsSourceParameters EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150682"
---
# <a name="credentialssourceparameters-complex-type"></a>Tipo complejo de CredentialsSourceParameters

El tipo complejo **CredentialsSourceParameters** define el elemento necesario para especificar el origen del certificado que se va a utilizar con una autenticación EAP-TLS.

Existe una opción entre el elemento de [**tarjeta inteligente**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) o el elemento [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) .

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                             | Tipo                                                                                  | Descripción                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | Indica que EAP-TLS debe leer el certificado del almacén My del usuario o el equipo que se va a autenticar. <br/> |
| [**Tarjeta**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [**emptyString**](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | Indica que EAP-TLS debe leer el certificado de la tarjeta inteligente. <br/>                                          |



## <a name="remarks"></a>Observaciones

Los elementos [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) y [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) no se pueden usar simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipos complejos de esquema de eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





