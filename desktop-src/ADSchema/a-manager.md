---
title: Atributo de administrador
description: Contiene el nombre distintivo del usuario que es el administrador del usuario. El objeto de usuario del administrador contiene una propiedad directReports que contiene referencias a todos los objetos de usuario que tienen sus propiedades de administrador establecidas en este nombre distintivo.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de administrador
- Esquema de AD del atributo de administrador
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b17f3252963e03c86b5b25a3651606a004afe672f1c8ec07f419ddff3a826
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301265"
---
# <a name="manager-attribute"></a>Atributo de administrador

Contiene el nombre distintivo del usuario que es el administrador del usuario. El objeto de usuario del administrador contiene una propiedad directReports que contiene referencias a todos los objetos de usuario que tienen sus propiedades de administrador establecidas en este nombre distintivo.



| Entrada | Valor |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Manager                                                                     |
| Ldap-Display-Name | manager                                                                     |
| Size              | \-                                                                          |
| Privilegio actualizar  | Administrador de dominio o propietario de la cuenta.                                      |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que el administrador necesita cambiar. |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| System-Id-Guid    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                                     |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------------------------------|
| Id. de vínculo                | 42                                                                 |
| MAPI-Id                | 0x8005                                                             |
| System-Only            | False                                                              |
| Es de un solo valor       | True                                                               |
| Está indexado             | False                                                              |
| En el catálogo global      | True                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Es de un solo valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Es de un solo valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Es de un solo valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Es de un solo valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Es de un solo valor       | True                                                                                                                   |
| Está indexado             | False                                                                                                                  |
| En el catálogo global      | True                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





