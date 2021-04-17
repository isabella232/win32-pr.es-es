---
description: Especifica el contexto de connenction de un dispositivo de banda ancha móvil.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: Tipo complejo de contextType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 63d221c6bd388196abfb73a8ac38a26de516d0df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659801"
---
# <a name="contexttype-complex-type"></a>Tipo complejo de contextType

El tipo complejo **contextType** especifica el contexto connenction de un dispositivo de banda ancha móvil.

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="UserName"
                        type="nameType"
                     />
                    <xs:element name="IgnorePassword"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo                                           | Descripción                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**AccessString**](schema-accessstring-contexttype-element.md)       |                                                | APN o cadena de marcado que se va a usar para establecer una conexión de datos<br/>                        |
| [**AuthProtocol**](schema-authprotocol-contexttype-element.md)       |                                                | Protocolo de autenticación que se va a usar para activar un contexto PDP.<br/>                    |
| [**Compresión**](schema-compression-contexttype-element.md)         |                                                | Especifica si se usará la compresión en el vínculo de datos para el encabezado y la transferencia de datos<br/> |
| [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md) | boolean                                        | Cómo administrar las contraseñas al actualizar perfiles.<br/>                                    |
| [**Contraseña**](schema-password-userlogoncred-element.md)             | string                                         | Contraseña usada para autenticar a un usuario<br/>                                                |
| [**UserLogonCred**](schema-userlogoncred-contexttype-element.md)     |                                                | Credenciales de inicio de sesión para una conexión.<br/>                                                |
| [**Nombre**](schema-username-userlogoncred-element.md)             | [**nameType**](schema-nametype-simpletype.md) | Nombre de usuario para el inicio de sesión<br/>                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



 

 




