---
title: Force-Logoff atributo
description: Se usa para calcular la hora de inicio en SamIGetAccountRestrictions. La hora de cierre de sesión menos Forzar cierre de sesión es igual a la hora de inicio.
ms.assetid: 2ce1d5db-52aa-49c5-aef2-ec67122100ed
ms.tgt_platform: multiple
keywords:
- Force-Logoff esquema de AD del atributo
- Esquema de AD del atributo forceLogoff
topic_type:
- apiref
api_name:
- Force-Logoff
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df1ab9721643edec3e03e91475c74e63dde94dcb982e0a84aad3cdf7c63b806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925855"
---
# <a name="force-logoff-attribute"></a>Force-Logoff atributo

Se usa para calcular la hora de inicio en SamIGetAccountRestrictions. La hora de cierre de sesión menos Forzar cierre de sesión es igual a la hora de inicio.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Force-Logoff                         |
| Ldap-Display-Name | forceLogoff                          |
| Size              | \-                                   |
| Privilegio actualizar  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.39                |
| System-Id-Guid    | bf967977-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervalo**](s-interval.md)       |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falso                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                     |
| Está indexado             | Falso                                                                                                    |
| En el catálogo global      | Falso                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falso                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                     |
| Está indexado             | Falso                                                                                                    |
| En el catálogo global      | Falso                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falso                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                     |
| Está indexado             | Falso                                                                                                    |
| En el catálogo global      | Falso                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falso                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                     |
| Está indexado             | Falso                                                                                                    |
| En el catálogo global      | Falso                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falso                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                     |
| Está indexado             | Falso                                                                                                    |
| En el catálogo global      | Falso                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falso                                                                                                    |
| Es de un solo valor       | Verdadero                                                                                                     |
| Está indexado             | Falso                                                                                                    |
| En el catálogo global      | Falso                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





