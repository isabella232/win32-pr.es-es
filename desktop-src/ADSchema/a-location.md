---
title: Location (atributo)
description: La ubicación del usuario, como el número de oficina.
ms.assetid: 3ee97a61-6dce-4f41-b03a-a475706f3cbd
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de ubicación
- esquema de AD de atributo de ubicación
topic_type:
- apiref
api_name:
- Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7e8080ffa24c9b2a147e6e3ec76f586a92fba3456aa1f80d2875c1292940232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705775"
---
# <a name="location-attribute-ad-schema"></a>Atributo Location (esquema de AD)

La ubicación del usuario, como el número de oficina.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Ubicación                                    |
| Ldap-Display-Name | ubicación                                    |
| Size              | \-                                          |
| Actualizar privilegios  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.222                      |
| System-Id-Guid    | 09dcb79f-165f-11d0-a064-00aa006c33ed        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                                                                             |
| Está indexado             | Verdadero                                                                                                                                                             |
| En el catálogo global      | Verdadero                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                |
| Range-Upper            | 1024                                                                                                                                                             |
| Search-Flags           | 0x00000001                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                       |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                                                                               |
| Está indexado             | Verdadero                                                                                                                                                                                               |
| En el catálogo global      | Verdadero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Habitación**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| Es de un solo valor       | Verdadero                                                                    |
| Está indexado             | Verdadero                                                                    |
| En el catálogo global      | Verdadero                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                            |
| Range-Lower            | 0                                                                       |
| Range-Upper            | 1024                                                                    |
| Search-Flags           | 0x00000001                                                              |
| System-Flags           | 0x00000010                                                              |
| Clases usadas en        | [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                                                                               |
| Está indexado             | Verdadero                                                                                                                                                                                               |
| En el catálogo global      | Verdadero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Habitación**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                                                                               |
| Está indexado             | Verdadero                                                                                                                                                                                               |
| En el catálogo global      | Verdadero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Habitación**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                                                                               |
| Está indexado             | Verdadero                                                                                                                                                                                               |
| En el catálogo global      | Verdadero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Habitación**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falso                                                                                                                                                                                              |
| Es de un solo valor       | Verdadero                                                                                                                                                                                               |
| Está indexado             | Verdadero                                                                                                                                                                                               |
| En el catálogo global      | Verdadero                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Habitación**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subred**](c-subnet.md)<br/> |



 

 





