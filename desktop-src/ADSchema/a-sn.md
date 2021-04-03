---
title: Atributo apellido
description: Este atributo contiene la familia o el apellido de un usuario.
ms.assetid: d9d53c9f-4efa-47c4-aec4-518fb8a868b3
ms.tgt_platform: multiple
keywords:
- Atributo de apellidos esquema de AD
- atributo SN del esquema de AD
topic_type:
- apiref
api_name:
- Surname
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453352574a7aec10c56492060ac2de6ceeca030f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997364"
---
# <a name="surname-attribute"></a>Atributo apellido

Este atributo contiene la familia o el apellido de un usuario.



| Entrada | Value |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Surname                                                                          |
| Nombre para mostrar de LDAP | sn                                                                               |
| Tamaño              | \-                                                                               |
| Actualizar privilegio  | Cualquier usuario puede actualizar este objeto en función de la seguridad del objeto que se va a crear. |
| Frecuencia de actualización  | \-                                                                               |
| Attribute-Id      | 2.5.4.4                                                                          |
| System-ID-GUID    | bf967a41-0de6-11d0-a285-00aa003049e2                                             |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|---------------------------------------|
| Identificador de vínculo                | \-                                    |
| MAPI-Id                | 0x3A11                                |
| System-Only            | False                                 |
| Tiene un único valor       | True                                  |
| Está indexado             | True                                  |
| En el catálogo global      | True                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 64                                    |
| Search-Flags           | 0x00000005                            |
| System-Flags           | 0x00000010                            |
| Clases usadas en        | [**Person**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | True                                                                                          |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | True                                                                                          |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | True                                                                                          |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | True                                                                                          |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | True                                                                                          |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





