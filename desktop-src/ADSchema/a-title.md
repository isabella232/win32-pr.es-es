---
title: Atributo Title
description: Contiene el título del trabajo del usuario. Esta propiedad se usa normalmente para indicar el puesto formal, como Programador sénior, en lugar de clase profesional, como el programador. Normalmente no se usa para los títulos de sufijo, como Esq. o DDS.
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de título
- title attribute AD Schema
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8885a557e8fbec17d6d58d68fdea0f99039f0e09e34a8da01954dc7b4979fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645035"
---
# <a name="title-attribute-ad-schema"></a>Atributo Title (esquema de AD)

Contiene el título del trabajo del usuario. Esta propiedad se usa normalmente para indicar el puesto formal, como Programador sénior, en lugar de clase profesional, como el programador. Normalmente no se usa para los títulos de sufijo, como Esq. o DDS.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------|
| CN                | Título                                                                     |
| Ldap-Display-Name | title                                                                     |
| Size              | \-                                                                        |
| Actualizar privilegios  | Administrador de dominio o propietario de la cuenta.                                    |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y siempre que el título necesita cambiar. |
| Attribute-Id      | 2.5.4.12                                                                  |
| System-Id-Guid    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                               |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Es de un solo valor       | Verdadero                                                                                                                            |
| Está indexado             | Falso                                                                                                                           |
| En el catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Es de un solo valor       | Verdadero                                                                                                                            |
| Está indexado             | Falso                                                                                                                           |
| En el catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Es de un solo valor       | Verdadero                                                                                                                            |
| Está indexado             | Falso                                                                                                                           |
| En el catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Es de un solo valor       | Verdadero                                                                                                                            |
| Está indexado             | Falso                                                                                                                           |
| En el catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Es de un solo valor       | Verdadero                                                                                                                            |
| Está indexado             | Falso                                                                                                                           |
| En el catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                              |
| MAPI-Id                | 0x3A17                                                                                                                          |
| System-Only            | Falso                                                                                                                           |
| Es de un solo valor       | Verdadero                                                                                                                            |
| Está indexado             | Falso                                                                                                                           |
| En el catálogo global      | Falso                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| Clases usadas en        | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> |



 

 





