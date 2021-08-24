---
title: Trust-Attributes atributo
description: Este atributo almacena los atributos de confianza para un dominio de confianza.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Trust-Attributes esquema de AD de atributo
- Esquema de AD del atributo trustAttributes
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d09104d0f32c770ba1fe3fbdde6cf56d56989a801856ba970284b2d06c96a5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704045"
---
# <a name="trust-attributes-attribute"></a>Trust-Attributes atributo

Este atributo almacena los atributos de confianza para un dominio de confianza. Los valores de atributo posibles son los siguientes:

-   TRUST \_ ATTRIBUTE \_ NON \_ TRANSITIVE Deshabilita la transitividad.
-   TRUST \_ ATTRIBUTE TREE PARENT Trust se establece en el elemento primario del árbol de la \_ \_ organización.
-   TRUST \_ ATTRIBUTE TREE ROOT Trust establecido en otra raíz de árbol en el \_ \_ bosque.
-   TRUST \_ ATTRIBUTE \_ UPLEVEL ONLY Vínculo de confianza válido solo \_ para el cliente de nivel superior.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Trust-Attributes                     |
| Ldap-Display-Name | trustAttributes                      |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.470               |
| System-Id-Guid    | 80a67e5a-9f22-11d0-afdd-00c04fd930c9 |
| Syntax            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
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



| Entrada | Value |
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



| Entrada | Value |
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



| Entrada | Value |
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



| Entrada | Value |
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



 

 





