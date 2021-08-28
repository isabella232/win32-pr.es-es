---
title: atributo dhcp-Type
description: Tipo de servidor DHCP.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo dhcp-Type
- Esquema de AD del atributo dhcpType
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f4cc64a05db9b88d13a1e7dfb3ce0976391b9d2514388ae9045eb11d97a5b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049655"
---
# <a name="dhcp-type-attribute"></a>atributo dhcp-Type

Tipo de servidor DHCP. Este atributo se establece en todos los objetos de objectClass [**dHCPClass**](c-dhcpclass.md). Su valor define el tipo de objeto:

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| Entrada | Value |
|-------------------|--------------------------------------------------------|
| CN                | dhcp-Type                                              |
| Ldap-Display-Name | dhcpType                                               |
| Size              | 4 bytes                                                |
| Privilegio actualizar  | Administrador de dominio.                                  |
| Frecuencia de actualización  | Cuando se agrega o quita un nuevo servidor del bosque. |
| Attribute-Id      | 1.2.840.113556.1.4.699                                 |
| System-Id-Guid    | 963d273b-48be-11d1-a9c3-0000f80367c1                   |
| Syntax            | [**Enumeración**](s-enumeration.md)                   |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Verdadero                                         |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**CLASE DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Verdadero                                         |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**CLASE DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Verdadero                                         |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**DHCP-Class**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Verdadero                                         |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**DHCP-Class**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Verdadero                                         |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**DHCP-Class**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Verdadero                                         |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**DHCP-Class**](c-dhcpclass.md)<br/> |



 

 





