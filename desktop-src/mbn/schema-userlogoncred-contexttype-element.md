---
description: Contiene credenciales de inicio de sesión para una conexión.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Elemento UserLogonCred (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475861"
---
# <a name="userlogoncred-contexttype-element"></a>Elemento UserLogonCred (contextType)

El **elemento UserLogonCred (contextType)** contiene credenciales de inicio de sesión para una conexión.

Este elemento puede tener los siguientes elementos secundarios.

-   [**Nombre de usuario**](schema-username-userlogoncred-element.md)
-   [**Contraseña**](schema-password-userlogoncred-element.md)
-   [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md)

Este elemento puede tener un máximo de una aparición.

Este elemento es opcional.

``` syntax
<xs:element name="UserLogonCred">
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
```

El **elemento UserLogonCred** se define mediante el [**tipo complejo contextType.**](schema-contexttype-complextype.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Tipo                                           | Descripción                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [**IgnorePassword**](schema-ignorepassword-userlogoncred-element.md) | boolean                                        | Cómo controlar contraseñas al actualizar perfiles.<br/> |
| [**Contraseña**](schema-password-userlogoncred-element.md)             | string                                         | Contraseña de usuario.<br/>                                   |
| [**Nombre de usuario**](schema-username-userlogoncred-element.md)             | [**nameType**](schema-nametype-simpletype.md) | Nombre de usuario.<br/>                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**Contexto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




