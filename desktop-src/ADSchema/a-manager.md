---
title: Atributo Manager
description: Contiene el nombre distintivo del usuario que es el administrador del usuario. El objeto de usuario del administrador contiene una propiedad directReports que contiene referencias a todos los objetos de usuario que tienen sus propiedades de administrador establecidas en este nombre distintivo.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Atributo de administrador esquema de AD
- atributo de administrador esquema de AD
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422689"
---
# <a name="manager-attribute"></a>Atributo Manager

Contiene el nombre distintivo del usuario que es el administrador del usuario. El objeto de usuario del administrador contiene una propiedad directReports que contiene referencias a todos los objetos de usuario que tienen sus propiedades de administrador establecidas en este nombre distintivo.



| Entrada | Value |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Manager                                                                     |
| Nombre para mostrar de LDAP | manager                                                                     |
| Tamaño              | \-                                                                          |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.                                      |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que el administrador tiene que cambiar. |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| System-ID-GUID    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
| Sintaxis            | [**Object(DS-DN)**](s-object-ds-dn.md)                                     |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|--------------------------------------------------------------------|
| Identificador de vínculo                | 42                                                                 |
| MAPI-Id                | 0x8005                                                             |
| System-Only            | False                                                              |
| Tiene un único valor       | True                                                               |
| Está indexado             | False                                                              |
| En el catálogo global      | True                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Tiene un único valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Tiene un único valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Tiene un único valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Tiene un único valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Tiene un único valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





