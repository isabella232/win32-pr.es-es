---
title: Atributo Other-Well-Known-Objects
description: Contiene una lista de contenedores por GUID y nombre distintivo. Esto permite recuperar un objeto después de que se haya movido usando solo el GUID y el nombre de dominio. Cada vez que se mueve el objeto, el sistema actualiza automáticamente el nombre distintivo.
ms.assetid: 2f33c4ac-235c-47a1-9340-5b90f7edb73b
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Other-Well-Known-Objects
- Esquema de AD del atributo otherWellKnownObjects
topic_type:
- apiref
api_name:
- Other-Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c56d8ca4de5928e8109b2503b57d1afce5909df484e607392543e85cfa63118c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923995"
---
# <a name="other-well-known-objects-attribute"></a>Atributo Other-Well-Known-Objects

Contiene una lista de contenedores por GUID y nombre distintivo. Esto permite recuperar un objeto después de que se haya movido usando solo el GUID y el nombre de dominio. Cada vez que se mueve el objeto, el sistema actualiza automáticamente el nombre distintivo.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Otros objetos well-known-objects                                                                                                                                                                                      |
| Ldap-Display-Name | otherWellKnownObjects                                                                                                                                                                                         |
| Size              | Ejemplo para recuperar el contenedor Users en el dominio microsoft: LDAP://(WKGUID=a9d1ca15768811d1aded00c04fd8d5cd,dc=microsoft,dc=com). NOTA: Corchetes angulares reemplazados por paréntesis para evitar conflictos XML. |
| Privilegio actualizar  | Administrador de esquemas                                                                                                                                                                                          |
| Frecuencia de actualización  | Siempre que se mueve el objeto.                                                                                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1359                                                                                                                                                                                       |
| System-Id-Guid    | 1ea64e5d-ac0f-11d2-90df-00c04fd91ab1                                                                                                                                                                          |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                                                                                               |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Falso                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



 

 





