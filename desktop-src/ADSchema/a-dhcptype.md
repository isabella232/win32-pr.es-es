---
title: atributo de tipo DHCP
description: El tipo de servidor DHCP.
ms.assetid: 46ab7db7-a752-45aa-a10b-1195b5cf6f80
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de tipo DHCP
- dhcpType esquema de AD de atributos
topic_type:
- apiref
api_name:
- dhcp-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5a5a331ff7298854f4ca070799a05e2a3497f2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997275"
---
# <a name="dhcp-type-attribute"></a>atributo de tipo DHCP

El tipo de servidor DHCP. Este atributo se establece en todos los objetos de objectClass [**dHCPClass**](c-dhcpclass.md). Su valor define el tipo de objeto:

``` syntax
  0 - DHCP Root Object
  1 - DHCP Server
```



| Entrada | Value |
|-------------------|--------------------------------------------------------|
| CN                | Tipo DHCP                                              |
| Nombre para mostrar de LDAP | dhcpType                                               |
| Tamaño              | 4 bytes                                                |
| Actualizar privilegio  | Administrador de dominio.                                  |
| Frecuencia de actualización  | Cuando se agrega o se quita un nuevo servidor del bosque. |
| Attribute-Id      | 1.2.840.113556.1.4.699                                 |
| System-ID-GUID    | 963d273b-48be-11d1-a9c3-0000f80367c1                   |
| Sintaxis            | [**Enumeración**](s-enumeration.md)                   |



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
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | True                                         |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**Clase de DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | True                                         |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**Clase de DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | True                                         |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**Clase de DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | True                                         |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**Clase de DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | True                                         |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**Clase de DHCP**](c-dhcpclass.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | True                                         |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000001                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**Clase de DHCP**](c-dhcpclass.md)<br/> |



 

 





