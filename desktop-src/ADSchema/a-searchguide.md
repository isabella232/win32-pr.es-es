---
title: Search-Guide atributo)
description: Especifica la información de los criterios de búsqueda sugeridos, que se pueden incluir en algunas entradas que se espera que sean un objeto base conveniente para la operación de búsqueda, por ejemplo, Country/region u Organization.
ms.assetid: 69823ef3-efa8-4732-bbec-27ed8fec81cc
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Search-Guide
- searchGuide esquema de AD de atributos
topic_type:
- apiref
api_name:
- Search-Guide
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711202ebc39649e7e1aea2a4459c3a7147eb2ff6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658745"
---
# <a name="search-guide-attribute"></a>Search-Guide atributo)

Especifica la información de los criterios de búsqueda sugeridos, que se pueden incluir en algunas entradas que se espera que sean un objeto base conveniente para la operación de búsqueda, por ejemplo, Country/region u Organization.



| Entrada | Value |
|-------------------|-------------------------------------------------------|
| CN                | Search-Guide                                          |
| Nombre para mostrar de LDAP | searchGuide                                           |
| Tamaño              | \-                                                    |
| Actualizar privilegio  | Administrador de dominio                                  |
| Frecuencia de actualización  | Siempre que se desee una nueva guía de búsqueda.               |
| Attribute-Id      | 2.5.4.14                                              |
| System-ID-GUID    | bf967a2e-0de6-11d0-a285-00aa003049e2                  |
| Sintaxis            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                                                                                                                                     |
| En el catálogo global      | False                                                                                                                                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                                                                                                                                     |
| En el catálogo global      | False                                                                                                                                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                 |
| MAPI-Id                | 0x812E                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                              |
| En el catálogo global      | False                                                                                                                                                                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| Clases usadas en        | [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                                                                                                                                     |
| En el catálogo global      | False                                                                                                                                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                                                                                                                                     |
| En el catálogo global      | False                                                                                                                                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                                                                                                                                     |
| En el catálogo global      | False                                                                                                                                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x812E                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                     |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                     |
| Está indexado             | False                                                                                                                                                                                                                                                                     |
| En el catálogo global      | False                                                                                                                                                                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                |
| Clases usadas en        | [**Entidad de certificación**](c-certificationauthority.md)<br/> [**País**](c-country.md)<br/> [**Localidad**](c-locality.md)<br/> [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



 

 





