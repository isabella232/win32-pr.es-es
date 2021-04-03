---
title: atributo MS-DS-Additional-DNS-host-name
description: El atributo se utiliza para almacenar el nombre de host DNS adicional de un objeto de equipo. Este atributo se usa en el momento en que se cambia el nombre de un controlador de dominio.
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre de host/DNS de MS-DS-Additional
- Esquema de AD de atributo msDS-AdditionalDnsHostName
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997447"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a>atributo MS-DS-Additional-DNS-host-name

El atributo se utiliza para almacenar el nombre de host DNS adicional de un objeto de equipo. Este atributo se utiliza en el momento en que se cambia el nombre de un equipo o los nombres se administran con "netdom computername".



| Entrada | Value |
|-------------------|-----------------------------------------------------------------------------|
| CN                | MS-DS-Additional-DNS-host-name                                              |
| Nombre para mostrar de LDAP | msDS-AdditionalDnsHostName                                                  |
| Tamaño              | Cada valor puede tener 2048 caracteres. El número de valor es el límite de la base de datos de aproximadamente 1200 valores. |
| Actualizar privilegio  | El sistema establece este valor.                                            |
| Frecuencia de actualización  | Cuando se cambia el nombre de un equipo.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1717                                                     |
| System-ID-GUID    | 80863791-dbe9-4eb8-837e-7f0ab55d9ac7                                        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------|
| Identificador de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Tiene un único valor       | False                                     |
| Está indexado             | False                                     |
| En el catálogo global      | False                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------|
| Identificador de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Tiene un único valor       | False                                     |
| Está indexado             | False                                     |
| En el catálogo global      | False                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------|
| Identificador de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Tiene un único valor       | False                                     |
| Está indexado             | False                                     |
| En el catálogo global      | False                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------|
| Identificador de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Tiene un único valor       | False                                     |
| Está indexado             | False                                     |
| En el catálogo global      | False                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------|
| Identificador de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Tiene un único valor       | False                                     |
| Está indexado             | False                                     |
| En el catálogo global      | False                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



 

 





