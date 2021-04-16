---
title: Dns-Root atributo)
description: El nombre de dominio DNS superior asignado a una partición de dominio o directorio.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Dns-Root
- dnsRoot esquema de AD de atributos
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658653"
---
# <a name="dns-root-attribute"></a>Dns-Root atributo)

El nombre de dominio DNS superior asignado a una partición de dominio o directorio. Se establece en un objeto crossRef y se usa, entre otras cosas, para la generación de referencias. Al buscar a través de un árbol de dominios completo, se debe iniciar la búsqueda en el objeto Dns-Root. Este atributo puede tener varios valores, en cuyo caso se generan varias referencias.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| Nombre para mostrar de LDAP | dnsRoot                                     |
| Tamaño              | \-                                          |
| Actualizar privilegio  | El sistema establece este valor.            |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| System-ID-GUID    | bf967959-0de6-11d0-a285-00aa003049e2        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|--------------------------------------------|
| Identificador de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Tiene un único valor       | False                                      |
| Está indexado             | True                                       |
| En el catálogo global      | False                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------|
| Identificador de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Tiene un único valor       | False                                      |
| Está indexado             | True                                       |
| En el catálogo global      | False                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------------------------------------|
| Identificador de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Tiene un único valor       | False                                      |
| Está indexado             | True                                       |
| En el catálogo global      | False                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------|
| Identificador de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Tiene un único valor       | False                                      |
| Está indexado             | True                                       |
| En el catálogo global      | False                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------|
| Identificador de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Tiene un único valor       | False                                      |
| Está indexado             | True                                       |
| En el catálogo global      | False                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------|
| Identificador de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Tiene un único valor       | False                                      |
| Está indexado             | True                                       |
| En el catálogo global      | False                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------|
| Identificador de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Tiene un único valor       | False                                      |
| Está indexado             | True                                       |
| En el catálogo global      | False                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



 

 





