---
title: Canonical-Name atributo)
description: Nombre del objeto en formato canónico.
ms.assetid: f217e5fa-f70b-4f4d-afa6-53e4f7e8a0e1
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Canonical-Name
- canonicalName esquema de AD de atributos
topic_type:
- apiref
api_name:
- Canonical-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 487476271456fa0465e8d47791f5376f33617eb9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906248"
---
# <a name="canonical-name-attribute"></a>Canonical-Name atributo)

Nombre del objeto en formato canónico. myserver2.fabrikam.com/users/jeffsmith es un ejemplo de un nombre distintivo en formato canónico. Este es un atributo construido. Los resultados devueltos son idénticos a los devueltos por la siguiente función de Active Directory: DsCrackNames (NULL, marca de nombre de DS \_ \_ \_ \_ solo sintáctica, \_ nombre de dominio completo de DS \_ 1779, nombre canónico de \_ DS \_ \_ ,...).

Para obtener más información sobre los formatos de nombre, vea [**DsCrackNames**](/windows/desktop/api/ntdsapi/nf-ntdsapi-dscracknamesa).



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Canonical-Name                              |
| Nombre para mostrar de LDAP | canonicalName                               |
| Tamaño              | \-                                          |
| Actualizar privilegio  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.916                      |
| System-ID-GUID    | 9a7ad945-ca53-11d1-bbd0-0080c76670c0        |
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
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | False                           |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



 

