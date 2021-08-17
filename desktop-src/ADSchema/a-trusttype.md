---
title: Trust-Type atributo
description: El tipo de confianza, por ejemplo, Windows NT o MIT.
ms.assetid: ad3640cd-d634-4ec1-8be8-1fb8272e4b23
ms.tgt_platform: multiple
keywords:
- Trust-Type esquema de AD de atributo
- Esquema de AD del atributo trustType
topic_type:
- apiref
api_name:
- Trust-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e3591117bb9ae89c0845aae41450812918d3dc3c88e6e31c3f4189f46ef8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681610"
---
# <a name="trust-type-attribute"></a>Trust-Type atributo

El tipo de confianza, por ejemplo, Windows NT o MIT.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Trust-Type                           |
| Ldap-Display-Name | trustType                            |
| Size              | 4 bytes                              |
| Actualizar privilegios  | El sistema establece este valor.     |
| Frecuencia de actualización  | Cuando se crea una nueva confianza.         |
| Attribute-Id      | 1.2.840.113556.1.4.136               |
| System-Id-Guid    | bf967a60-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Verdadero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Verdadero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Verdadero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Verdadero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| Id. de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Es de un solo valor       | Verdadero                                                 |
| Está indexado             | Falso                                                |
| En el catálogo global      | Verdadero                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



 

 





