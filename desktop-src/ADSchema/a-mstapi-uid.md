---
title: atributo de identificador único de MS-TAPI
description: Proporciona el nombre de una conferencia de multidifusión de TAPI. Es el atributo de nomenclatura de la clase Rt-Conference.
ms.assetid: a8162af7-0169-4381-8edc-3dbbf178e8ed
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de identificador único de MS-TAPI
- msTAPI-UID atributo AD Schema
topic_type:
- apiref
api_name:
- ms-TAPI-Unique-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 528d34d9d4282dac3f5bd5a41231094fd2666c2c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422675"
---
# <a name="ms-tapi-unique-identifier-attribute"></a>atributo de identificador único de MS-TAPI

Proporciona el nombre de una conferencia de multidifusión de TAPI. Es el atributo de nomenclatura de la clase Rt-Conference.



| Entrada | Value |
|-------------------|-----------------------------------------------------------------------|
| CN                | Identificador único de MS-TAPI                                             |
| Nombre para mostrar de LDAP | msTAPI: UID                                                            |
| Tamaño              | Puede ser una cadena arbitraria, normalmente menos de 100 caracteres de longitud. |
| Actualizar privilegio  | No se requieren privilegios especiales.                                       |
| Frecuencia de actualización  | Se establece una vez en el momento de crear el objeto de Rt-Conference.            |
| Attribute-Id      | 1.2.840.113556.1.4.1698                                               |
| System-ID-GUID    | 70a4e7ea-b3b9-4643-8918-e6dd2471bfd4                                  |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                           |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Tiene un único valor       | True                                                                                                                        |
| Está indexado             | False                                                                                                                       |
| En el catálogo global      | False                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Clases usadas en        | [**Microsoft-TAPI-RT-Conference**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-persona**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Tiene un único valor       | True                                                                                                                        |
| Está indexado             | False                                                                                                                       |
| En el catálogo global      | False                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Clases usadas en        | [**Microsoft-TAPI-RT-Conference**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-persona**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Tiene un único valor       | True                                                                                                                        |
| Está indexado             | False                                                                                                                       |
| En el catálogo global      | False                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Clases usadas en        | [**Microsoft-TAPI-RT-Conference**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-persona**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Tiene un único valor       | True                                                                                                                        |
| Está indexado             | False                                                                                                                       |
| En el catálogo global      | False                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Clases usadas en        | [**Microsoft-TAPI-RT-Conference**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-persona**](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                          |
| MAPI-Id                | \-                                                                                                                          |
| System-Only            | False                                                                                                                       |
| Tiene un único valor       | True                                                                                                                        |
| Está indexado             | False                                                                                                                       |
| En el catálogo global      | False                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                |
| Range-Lower            | \-                                                                                                                          |
| Range-Upper            | \-                                                                                                                          |
| Search-Flags           | 0x00000000                                                                                                                  |
| System-Flags           | 0x00000010                                                                                                                  |
| Clases usadas en        | [**Microsoft-TAPI-RT-Conference**](c-mstapi-rtconference.md)<br/> [**MS-TAPI-RT-persona**](c-mstapi-rtperson.md)<br/> |



 

 





