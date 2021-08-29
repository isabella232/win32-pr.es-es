---
title: Country-Code atributo
description: Especifica el código de país o región para el idioma que elija el usuario. No usa este valor Windows 2000.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- Country-Code esquema de AD de atributo
- CountryCode attribute AD Schema (Esquema de AD del atributo countryCode)
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7843a2724043e504538ad6388e92dfc205463e76e082c266b5ee1f4f095207ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961784"
---
# <a name="country-code-attribute"></a>Country-Code atributo

Especifica el código de país o región para el idioma que elija el usuario. No usa este valor Windows 2000.



| Entrada | Value |
|-------------------|-----------------------------------------|
| CN                | Country-Code                            |
| Ldap-Display-Name | countryCode                             |
| Size              | 2 bytes                                 |
| Actualizar privilegios  | Propietario de la cuenta o administrador de dominio   |
| Frecuencia de actualización  | Cuando cambia el país o región del usuario. |
| Attribute-Id      | 1.2.840.113556.1.4.25                   |
| System-Id-Guid    | 5fd42471-1262-11d0-a060-00aa006c33ed    |
| Syntax            | [**Enumeración**](s-enumeration.md)    |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                                              |
| Está indexado             | Falso                                                                                                                             |
| En el catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                      |
| Range-Lower            | \-                                                                                                                                |
| Range-Upper            | \-                                                                                                                                |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                                              |
| Está indexado             | Falso                                                                                                                             |
| En el catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|----------------------------------------------------------------|
| Id. de vínculo                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | Falso                                                          |
| Es de un solo valor       | Verdadero                                                           |
| Está indexado             | Falso                                                          |
| En el catálogo global      | Falso                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 65535                                                          |
| Search-Flags           | 0x00000010                                                     |
| System-Flags           | 0x00000010                                                     |
| Clases usadas en        | [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                                              |
| Está indexado             | Falso                                                                                                                             |
| En el catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                                              |
| Está indexado             | Falso                                                                                                                             |
| En el catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                                              |
| Está indexado             | Falso                                                                                                                             |
| En el catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | Falso                                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                                              |
| Está indexado             | Falso                                                                                                                             |
| En el catálogo global      | Falso                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



 

 





