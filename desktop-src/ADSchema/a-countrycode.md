---
title: Country-Code atributo)
description: Especifica el código de país o región para el idioma de elección del usuario. Windows 2000 no usa este valor.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Country-Code
- countryCode atributo AD Schema
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659214"
---
# <a name="country-code-attribute"></a>Country-Code atributo)

Especifica el código de país o región para el idioma de elección del usuario. Windows 2000 no usa este valor.



| Entrada | Value |
|-------------------|-----------------------------------------|
| CN                | Country-Code                            |
| Nombre para mostrar de LDAP | countryCode                             |
| Tamaño              | 2 bytes                                 |
| Actualizar privilegio  | Propietario de la cuenta o administrador de dominio   |
| Frecuencia de actualización  | Cuando cambia el país o la región del usuario. |
| Attribute-Id      | 1.2.840.113556.1.4.25                   |
| System-ID-GUID    | 5fd42471-1262-11d0-a060-00aa006c33ed    |
| Sintaxis            | [**Enumeración**](s-enumeration.md)    |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Tiene un único valor       | True                                                                                                                              |
| Está indexado             | False                                                                                                                             |
| En el catálogo global      | False                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                      |
| Range-Lower            | \-                                                                                                                                |
| Range-Upper            | \-                                                                                                                                |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Tiene un único valor       | True                                                                                                                              |
| Está indexado             | False                                                                                                                             |
| En el catálogo global      | False                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|----------------------------------------------------------------|
| Identificador de vínculo                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | False                                                          |
| Tiene un único valor       | True                                                           |
| Está indexado             | False                                                          |
| En el catálogo global      | False                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 65535                                                          |
| Search-Flags           | 0x00000010                                                     |
| System-Flags           | 0x00000010                                                     |
| Clases usadas en        | [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Tiene un único valor       | True                                                                                                                              |
| Está indexado             | False                                                                                                                             |
| En el catálogo global      | False                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Tiene un único valor       | True                                                                                                                              |
| Está indexado             | False                                                                                                                             |
| En el catálogo global      | False                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Tiene un único valor       | True                                                                                                                              |
| Está indexado             | False                                                                                                                             |
| En el catálogo global      | False                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Tiene un único valor       | True                                                                                                                              |
| Está indexado             | False                                                                                                                             |
| En el catálogo global      | False                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



 

 





