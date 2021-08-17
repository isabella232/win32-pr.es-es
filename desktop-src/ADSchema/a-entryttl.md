---
title: Atributo Entry-TTL
description: El servidor mantiene este atributo operativo y parece estar presente en cada entrada dinámica.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Entry-TTL
- Esquema de AD del atributo entryTTL
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcd3e06304824ba51431b00b6a5b90d24d7719194dd84974470a101d5f6a1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961564"
---
# <a name="entry-ttl-attribute"></a>Atributo Entry-TTL

El servidor mantiene este atributo operativo y parece estar presente en cada entrada dinámica. El atributo no está presente cuando la entrada no contiene la clase de objeto dynamicObject. El valor de este atributo es el tiempo, en segundos, que la entrada seguirá existiendo antes de desaparecer del directorio. En ausencia de operaciones de "actualización" que intervienen, se garantiza que los valores devueltos al leer el atributo en dos búsquedas sucesivas no sean decrecientes. El valor permitido más pequeño es 0, lo que indica que la entrada puede desaparecer sin previo aviso. El atributo está marcado como NO-USER-MODIFICATION porque solo se puede cambiar mediante la operación de actualización.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Entry-TTL                                   |
| Ldap-Display-Name | entryTTL                                    |
| Size              | 4 bytes. Máximo = 1 año, valor predeterminado = 1 día. |
| Actualizar privilegios  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.3.6.1.4.1.1466.101.119.3                  |
| System-Id-Guid    | d213decc-d81a-4384-aac2-dcfcfd631cf8        |
| Syntax            | [**Enumeración**](s-enumeration.md)        |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Clases usadas en        | [**Dynamic-Object**](c-dynamicobject.md)<br/> |



 

 





