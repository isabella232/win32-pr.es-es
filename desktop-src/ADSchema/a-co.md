---
title: Text-Country atributo)
description: El país o la región donde se encuentra el usuario.
ms.assetid: 6024de35-9ab5-4e03-97dc-0ebf830e5754
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Text-Country
- atributo de co-esquema de AD
topic_type:
- apiref
api_name:
- Text-Country
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f208ffe60e968632b6f90b534a5240c85f819587
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805107"
---
# <a name="text-country-attribute"></a>Text-Country atributo)

El país o la región donde se encuentra el usuario.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Text-Country                                |
| Nombre para mostrar de LDAP | co                                          |
| Tamaño              | \-                                          |
| Actualizar privilegio  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.2.131                      |
| System-ID-GUID    | f0f8ffa7-1191-11d0-a060-00aa006c33ed        |
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
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                        |
| MAPI-Id                | 0x3A26                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                     |
| Tiene un único valor       | True                                                                                                                                                                      |
| Está indexado             | False                                                                                                                                                                     |
| En el catálogo global      | False                                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                |
| Clases usadas en        | [**País**](c-country.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                             |
| Tiene un único valor       | True                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                             |
| En el catálogo global      | False                                                                                                                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Clases usadas en        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                     |
| MAPI-Id                | 0x3A26                                                                                                 |
| System-Only            | False                                                                                                  |
| Tiene un único valor       | True                                                                                                   |
| Está indexado             | False                                                                                                  |
| En el catálogo global      | False                                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                           |
| Range-Lower            | 1                                                                                                      |
| Range-Upper            | 128                                                                                                    |
| Search-Flags           | 0x00000010                                                                                             |
| System-Flags           | 0x00000010                                                                                             |
| Clases usadas en        | [**País**](c-country.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                             |
| Tiene un único valor       | True                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                             |
| En el catálogo global      | False                                                                                                                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Clases usadas en        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                             |
| Tiene un único valor       | True                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                             |
| En el catálogo global      | False                                                                                                                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Clases usadas en        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                             |
| Tiene un único valor       | True                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                             |
| En el catálogo global      | False                                                                                                                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Clases usadas en        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                |
| MAPI-Id                | 0x3A26                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                             |
| Tiene un único valor       | True                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                             |
| En el catálogo global      | False                                                                                                                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                 |
| Range-Upper            | 128                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                                                                                                                        |
| Clases usadas en        | [**País**](c-country.md)<br/> [**friendlyCountry**](c-friendlycountry.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



 

 





