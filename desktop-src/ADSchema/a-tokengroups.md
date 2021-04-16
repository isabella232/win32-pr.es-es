---
title: Token-Groups atributo)
description: Un atributo calculado que contiene la lista de SID debido a una operación de expansión de pertenencia a grupos transitiva en un usuario o equipo determinado. No se pueden recuperar grupos de tokens si no hay ningún catálogo global presente para recuperar las pertenencias inversas transitivas.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Token-Groups
- tokenGroups esquema de AD de atributos
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5342d1ff2bf549796340532b0514d5c5b060c2c1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658727"
---
# <a name="token-groups-attribute"></a>Token-Groups atributo)

Un atributo calculado que contiene la lista de SID debido a una operación de expansión de pertenencia a grupos transitiva en un usuario o equipo determinado. No se pueden recuperar grupos de tokens si no hay ningún catálogo global presente para recuperar las pertenencias inversas transitivas.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Token-Groups                         |
| Nombre para mostrar de LDAP | tokenGroups                          |
| Tamaño              | \-                                   |
| Actualizar privilegio  | El sistema establece este valor.     |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1301              |
| System-ID-GUID    | b7c69e6d-2cc7-11d2-854e-00a0c983f608 |
| Sintaxis            | [**Cadena (SID)**](s-string-sid.md)  |



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
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | False                                                        |
| En el catálogo global      | False                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | False                                                        |
| En el catálogo global      | False                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | False                                                        |
| En el catálogo global      | False                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | False                                                        |
| En el catálogo global      | False                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | False                                                        |
| En el catálogo global      | False                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | False                                                        |
| En el catálogo global      | False                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | False                                                        |
| En el catálogo global      | False                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





