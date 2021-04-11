---
title: Location (atributo)
description: La ubicación del usuario, como el número de oficina.
ms.assetid: 3ee97a61-6dce-4f41-b03a-a475706f3cbd
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de ubicación
- Esquema de AD de atributo de ubicación
topic_type:
- apiref
api_name:
- Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a37f15e80d470c0662036745f285aea87e79391
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151691"
---
# <a name="location-attribute-ad-schema"></a>Location (atributo) (esquema de AD)

La ubicación del usuario, como el número de oficina.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Location                                    |
| Nombre para mostrar de LDAP | ubicación                                    |
| Tamaño              | \-                                          |
| Actualizar privilegio  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.222                      |
| System-ID-GUID    | 09dcb79f-165f-11d0-a064-00aa006c33ed        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                               |
| System-Only            | False                                                                                                                                                            |
| Tiene un único valor       | True                                                                                                                                                             |
| Está indexado             | True                                                                                                                                                             |
| En el catálogo global      | True                                                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                |
| Range-Upper            | 1024                                                                                                                                                             |
| Search-Flags           | 0x00000001                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                       |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                                                                               |
| Está indexado             | True                                                                                                                                                                                               |
| En el catálogo global      | True                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**misma**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | False                                                                   |
| Tiene un único valor       | True                                                                    |
| Está indexado             | True                                                                    |
| En el catálogo global      | True                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                            |
| Range-Lower            | 0                                                                       |
| Range-Upper            | 1024                                                                    |
| Search-Flags           | 0x00000001                                                              |
| System-Flags           | 0x00000010                                                              |
| Clases usadas en        | [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                                                                               |
| Está indexado             | True                                                                                                                                                                                               |
| En el catálogo global      | True                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**misma**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                                                                               |
| Está indexado             | True                                                                                                                                                                                               |
| En el catálogo global      | True                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**misma**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                                                                               |
| Está indexado             | True                                                                                                                                                                                               |
| En el catálogo global      | True                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**misma**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Tiene un único valor       | True                                                                                                                                                                                               |
| Está indexado             | True                                                                                                                                                                                               |
| En el catálogo global      | True                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**misma**](c-room.md)<br/> [**Sitio**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



 

 





