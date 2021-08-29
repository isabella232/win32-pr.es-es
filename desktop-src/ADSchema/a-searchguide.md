---
title: Search-Guide atributo
description: Especifica información de los criterios de búsqueda sugeridos, que pueden incluirse en algunas entradas que se espera que sean un objeto base conveniente para la operación de búsqueda, por ejemplo, país o región u organización.
ms.assetid: 69823ef3-efa8-4732-bbec-27ed8fec81cc
ms.tgt_platform: multiple
keywords:
- Search-Guide esquema de AD del atributo
- SearchGuide attribute AD Schema (Esquema de AD del atributo searchGuide)
topic_type:
- apiref
api_name:
- Search-Guide
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aedd7e97716766f9dc0bb264df6d82ecfdb18951df135c5329898b86ae866a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836965"
---
# <a name="search-guide-attribute"></a>Search-Guide atributo

Especifica información de los criterios de búsqueda sugeridos, que pueden incluirse en algunas entradas que se espera que sean un objeto base conveniente para la operación de búsqueda, por ejemplo, país o región u organización.



| Entrada | Value |
|-------------------|-------------------------------------------------------|
| CN                | Search-Guide                                          |
| Ldap-Display-Name | searchGuide                                           |
| Size              | \-                                                    |
| Privilegio actualizar  | Administrador de dominio                                  |
| Frecuencia de actualización  | Siempre que se desee una nueva guía de búsqueda.               |
| Attribute-Id      | 2.5.4.14                                              |
| System-Id-Guid    | bf967a2e-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | 0x812E                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                              |
| En el catálogo global      | Falso                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                                                                                                                     |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                                                                                                                                     |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



 

 





