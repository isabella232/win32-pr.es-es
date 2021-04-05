---
title: Options (atributo)
description: Un campo de bits, donde el significado de los bits varía de objectClass a objectClass. Puede producirse en el transporte entre sitios, NTDS-Connection, NTDS-DSA, NTDS-Site-Settings y Site-Link objetos.
ms.assetid: 07495cc1-1db0-4e0d-afbe-b21d2b50b6a1
ms.tgt_platform: multiple
keywords:
- Atributo de opciones esquema de AD
- atributo de opciones esquema de AD
topic_type:
- apiref
api_name:
- Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd970a805816e941c9eb017bf6b96302eef2b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493744"
---
# <a name="options-attribute"></a>Options (atributo)

Un campo de bits, donde el significado de los bits varía de objectClass a objectClass. Puede producirse en el transporte entre sitios, NTDS-Connection, NTDS-DSA, NTDS-Site-Settings y Site-Link objetos.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Opciones                              |
| Nombre para mostrar de LDAP | opciones                              |
| Tamaño              | 4 bytes                              |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.307               |
| System-ID-GUID    | 19195a53-6da0-11d0-afd3-00c04fd930c9 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                  |
| En el catálogo global      | False                                                                                                                                                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                  |
| En el catálogo global      | False                                                                                                                                                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                  |
| En el catálogo global      | False                                                                                                                                                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                  |
| En el catálogo global      | False                                                                                                                                                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                  |
| En el catálogo global      | False                                                                                                                                                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                  |
| En el catálogo global      | False                                                                                                                                                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                   |
| Está indexado             | False                                                                                                                                                                                                                                                                  |
| En el catálogo global      | False                                                                                                                                                                                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



 

 





