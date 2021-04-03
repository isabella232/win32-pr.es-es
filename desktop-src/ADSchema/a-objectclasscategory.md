---
title: Atributo Object-Class-Category
description: Este atributo contiene el tipo de clase, como abstract, auxiliar o estructurado.
ms.assetid: 0698392d-991e-4a3c-b734-54d025a38d50
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de clase de objeto y categoría
- objectClassCategory esquema de AD de atributos
topic_type:
- apiref
api_name:
- Object-Class-Category
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397bb50e0af0c9dcddcc535d0bcddb1c8d525cfc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997380"
---
# <a name="object-class-category-attribute"></a>Atributo Object-Class-Category

Este atributo contiene el tipo de clase, como abstract, auxiliar o estructurado.



| Entrada | Value |
|-------------------|---------------------------------------------------------------------------------|
| CN                | Objeto-clase-categoría                                                           |
| Nombre para mostrar de LDAP | objectClassCategory                                                             |
| Tamaño              | 4 bytes. Estructural 1, abstract 2, auxiliar 3. No se debe usar la clase 88, 0. |
| Actualizar privilegio  | El diseñador del objeto establecería este valor.                                |
| Frecuencia de actualización  | Este valor no debe cambiar nunca.                                                 |
| Attribute-Id      | 1.2.840.113556.1.2.370                                                          |
| System-ID-GUID    | bf9679e6-0de6-11d0-a285-00aa003049e2                                            |
| Sintaxis            | [**Enumeración**](s-enumeration.md)                                            |



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
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x80F6                                           |
| System-Only            | True                                             |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 3                                                |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**Esquema de clase**](c-classschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x80F6                                           |
| System-Only            | True                                             |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 3                                                |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**Esquema de clase**](c-classschema.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x80F6                                           |
| System-Only            | True                                             |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 3                                                |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**Esquema de clase**](c-classschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x80F6                                           |
| System-Only            | True                                             |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 3                                                |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**Esquema de clase**](c-classschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x80F6                                           |
| System-Only            | True                                             |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 3                                                |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**Esquema de clase**](c-classschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x80F6                                           |
| System-Only            | True                                             |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 3                                                |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**Esquema de clase**](c-classschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x80F6                                           |
| System-Only            | True                                             |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | 0                                                |
| Range-Upper            | 3                                                |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**Esquema de clase**](c-classschema.md)<br/> |



 

 





