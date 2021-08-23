---
title: Atributo Initials
description: Contiene las iniciales de partes del nombre completo del usuario. Esto se puede usar como inicial central en la Windows de direcciones.
ms.assetid: 220b4448-5276-4c3f-8a1b-217cec06135a
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Initials
- Esquema de AD del atributo initials
topic_type:
- apiref
api_name:
- Initials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c9aa6020dc5f442547582c71be475c7dc8e6e3efcd3e1588095c536f22e2347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322915"
---
# <a name="initials-attribute"></a>Atributo Initials

Contiene las iniciales de partes del nombre completo del usuario. Esto se puede usar como inicial central en la Windows de direcciones.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Iniciales                                    |
| Ldap-Display-Name | Initials                                    |
| Size              | \-                                          |
| Actualizar privilegios  | Administrador de dominio o propietario de la cuenta.      |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 2.5.4.43                                    |
| System-Id-Guid    | f0f8ff90-1191-11d0-a060-00aa006c33ed        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
| Id. de vínculo                | \-                                                                 |
| MAPI-Id                | 0x3A0A                                                             |
| System-Only            | Falso                                                              |
| Es de un solo valor       | Verdadero                                                               |
| Está indexado             | Falso                                                              |
| En el catálogo global      | Falso                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 6                                                                  |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Falso                                                                                                                  |
| En el catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Falso                                                                                                                  |
| En el catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Falso                                                                                                                  |
| En el catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Falso                                                                                                                  |
| En el catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                     |
| MAPI-Id                | 0x3A0A                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Es de un solo valor       | Verdadero                                                                                                                   |
| Está indexado             | Falso                                                                                                                  |
| En el catálogo global      | Falso                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 1                                                                                                                      |
| Range-Upper            | 6                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





