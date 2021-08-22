---
title: Token-Groups atributo
description: Atributo calculado que contiene la lista de SID debido a una operación transitiva de expansión de pertenencia a grupos en un usuario o equipo determinado. Los grupos de tokens no se pueden recuperar si no hay ningún catálogo global para recuperar las pertenencias inversas transitivas.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Token-Groups esquema de AD del atributo
- Esquema de AD del atributo tokenGroups
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8971f9ba5baead73b7704760dcc86430f5ce1a318ac6bcbd9dfaf4125a21af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022073"
---
# <a name="token-groups-attribute"></a>Token-Groups atributo

Atributo calculado que contiene la lista de SID debido a una operación transitiva de expansión de pertenencia a grupos en un usuario o equipo determinado. Los grupos de tokens no se pueden recuperar si no hay ningún catálogo global para recuperar las pertenencias inversas transitivas.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Token-Groups                         |
| Ldap-Display-Name | tokenGroups                          |
| Size              | \-                                   |
| Privilegio actualizar  | El sistema establece este valor.     |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1301              |
| System-Id-Guid    | b7c69e6d-2cc7-11d2-854e-00a0c983f608 |
| Syntax            | [**String(Sid)**](s-string-sid.md)  |



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
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Falso                                                        |
| En el catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Falso                                                        |
| En el catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Falso                                                        |
| En el catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Falso                                                        |
| En el catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Falso                                                        |
| En el catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Falso                                                        |
| En el catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Falso                                                        |
| En el catálogo global      | Falso                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





