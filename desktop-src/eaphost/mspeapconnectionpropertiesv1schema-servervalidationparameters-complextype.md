---
title: Tipo complejo de ServerValidationParameters (PEAP)
description: Obtenga información sobre el tipo complejo de ServerValidationParameters. Este tipo contiene información sobre cómo realizar la validación del servidor. | Tipo complejo de ServerValidationParameters (PEAP)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
keywords:
- Tipo complejo ServerValidationParameters EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003506"
---
# <a name="servervalidationparameters-complex-type-peap"></a>Tipo complejo de ServerValidationParameters (PEAP)

El tipo complejo **ServerValidationParameters** contiene información sobre cómo realizar la validación del servidor.

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                                                                    | Tipo        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | boolean     | Indica si se debe solicitar al usuario la validación del servidor. <br/> Si [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) es true, PEAP realiza la validación del servidor sin intervención del usuario; Si se produce un error en la validación, PEAP produce un error en la autenticación.<br/> Si [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) es false, se solicita al usuario un certificado o un nombre de servidor validados, o una entidad de certificación raíz (CA).<br/> El elemento [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) es opcional.<br/> |
| [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | complexType | Representa una lista de servidores en los que el cliente confía. Cada nombre de servidor está delimitado por punto y coma, y se puede representar mediante expresiones regulares. <br/> El elemento [**servernames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | hexBinary   | Captura la impresión en miniatura de las entidades de certificación (CA) raíz en las que confía el cliente. <br/> La impresión en miniatura es una cadena hexadecimal que contiene el hash SHA-1 del certificado.<br/> El elemento [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a>Atributos



| Nombre                    | Tipo    | Descripción                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PerformServerValidation | boolean | Windows 7 o posterior: indica si se realiza la validación del servidor. El elemento [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) es opcional.<br/> |



## <a name="requirements"></a>Requisitos



| Role | Versión mínima admitida del sistema operativo |
|------|------------------------------|
| Remoto<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[EAPHost y esquema heredado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipos complejos de esquema de mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[**AcceptServerName**](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





