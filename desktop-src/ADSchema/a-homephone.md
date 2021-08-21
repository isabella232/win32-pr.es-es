---
title: Teléfono-Home-Primary
description: Número de teléfono principal del usuario.
ms.assetid: 624d89fd-942c-448d-bd51-7d93954370b1
ms.tgt_platform: multiple
keywords:
- Teléfono esquema de AD de atributo principal-principal de Teléfono inicio
- Esquema de AD del atributo homePhone
topic_type:
- apiref
api_name:
- Phone-Home-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 321ba35912db00e8b33f840d73cd68010166c7e38a19e6b6a43e64bc886a8496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118176714"
---
# <a name="phone-home-primary-attribute"></a>Teléfono-Home-Primary

Número de teléfono principal del usuario.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Teléfono-Home-Primary                                                               |
| Ldap-Display-Name | homePhone                                                                        |
| Size              | \-                                                                               |
| Actualizar privilegios  | Administrador de dominio o propietario de la cuenta.                                           |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y siempre que sea necesario cambiar el número de teléfono. |
| Attribute-Id      | 0.9.2342.19200300.100.1.20                                                       |
| System-Id-Guid    | f0f8ffa1-1191-11d0-a060-00aa006c33ed                                             |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                      |



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
| Id. de vínculo                | \-                                                                 |
| MAPI-Id                | 0x3A09                                                             |
| System-Only            | Falso                                                              |
| Es de un solo valor       | Verdadero                                                               |
| Está indexado             | Falso                                                              |
| En el catálogo global      | Verdadero                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                                                                     |
| Está indexado             | Falso                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Usuario**](c-user.md)<br/> |



 

 





