---
title: Atributo DNS-host-name
description: Nombre del equipo registrado en DNS.
ms.assetid: ba655adb-cb70-47f2-820f-c5b0749d3e70
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de nombre de host DNS
- Esquema de AD del atributo dNSHostName
topic_type:
- apiref
api_name:
- DNS-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7580a58e5d3042633a9dd665354bc883b4fdb87c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535764"
---
# <a name="dns-host-name-attribute"></a>Atributo DNS-host-name

Nombre del equipo registrado en DNS.



| Entrada | Value |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Nombre del host DNS                                                               |
| Nombre para mostrar de LDAP | dNSHostName                                                                 |
| Tamaño              | Cada segmento puede tener 63 caracteres. La longitud completa puede ser de 255 caracteres. |
| Actualizar privilegio  | Administrador de dominio                                                        |
| Frecuencia de actualización  | Cuando el equipo se denomina.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.619                                                      |
| System-ID-GUID    | 72e39547-7b18-11d1-adef-00c04fd8d5cd                                        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Tiene un único valor       | True                                                                                                                                                                                                                       |
| Está indexado             | False                                                                                                                                                                                                                      |
| En el catálogo global      | True                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Tiene un único valor       | True                                                                                                                                                                                                                       |
| Está indexado             | False                                                                                                                                                                                                                      |
| En el catálogo global      | True                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------------|
| Identificador de vínculo                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | False                                 |
| Tiene un único valor       | True                                  |
| Está indexado             | False                                 |
| En el catálogo global      | True                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                          |
| Range-Lower            | 0                                     |
| Range-Upper            | 2048                                  |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Clases usadas en        | [**Server**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Tiene un único valor       | True                                                                                                                                                                                                                       |
| Está indexado             | False                                                                                                                                                                                                                      |
| En el catálogo global      | True                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Tiene un único valor       | True                                                                                                                                                                                                                       |
| Está indexado             | False                                                                                                                                                                                                                      |
| En el catálogo global      | True                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Tiene un único valor       | True                                                                                                                                                                                                                       |
| Está indexado             | False                                                                                                                                                                                                                      |
| En el catálogo global      | True                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Server**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | False                                                                                                                                                                                                                      |
| Tiene un único valor       | True                                                                                                                                                                                                                       |
| Está indexado             | False                                                                                                                                                                                                                      |
| En el catálogo global      | True                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



 

 





