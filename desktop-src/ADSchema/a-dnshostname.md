---
title: Atributo DNS-Host-Name
description: Nombre del equipo registrado en DNS.
ms.assetid: ba655adb-cb70-47f2-820f-c5b0749d3e70
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo DNS-Host-Name
- Esquema de AD del atributo dNSHostName
topic_type:
- apiref
api_name:
- DNS-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241ea7144db7895e521c2844627d77b2f0ce54b5da518d180c87c6e9f834140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085965"
---
# <a name="dns-host-name-attribute"></a>Atributo DNS-Host-Name

Nombre del equipo registrado en DNS.



| Entrada | Value |
|-------------------|-----------------------------------------------------------------------------|
| CN                | DNS-Host-Name                                                               |
| Ldap-Display-Name | dNSHostName                                                                 |
| Size              | Cada segmento puede tener 63 caracteres. La longitud completa puede ser de 255 caracteres. |
| Privilegio actualizar  | Administrador de dominio                                                        |
| Frecuencia de actualización  | Cuando se denomina el equipo.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.619                                                      |
| System-Id-Guid    | 72e39547-7b18-11d1-adef-00c04fd8d5cd                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|---------------------------------------|
| Id. de vínculo                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Es de un solo valor       | Verdadero                                  |
| Está indexado             | Falso                                 |
| En el catálogo global      | Verdadero                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                          |
| Range-Lower            | 0                                     |
| Range-Upper            | 2048                                  |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000010                            |
| Clases usadas en        | [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                         |
| MAPI-Id                | \-                                                                                                                                                                                                                         |
| System-Only            | Falso                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                       |
| Está indexado             | Falso                                                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                          |
| Range-Upper            | 2048                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**Computer**](c-computer.md)<br/> [**PKI-Enrollment-Service**](c-pkienrollmentservice.md)<br/> [**Servidor**](c-server.md)<br/> |



 

 





