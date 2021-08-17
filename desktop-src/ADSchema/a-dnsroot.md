---
title: Dns-Root atributo
description: Nombre de dominio DNS superior asignado a una partición de dominio o directorio.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Dns-Root esquema de AD de atributo
- Esquema de AD del atributo dnsRoot
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f87acecb86fcd8ca8af4bbc2917dbe5381deaf4e5722a5803d31f186e57e04d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961584"
---
# <a name="dns-root-attribute"></a>Dns-Root atributo

Nombre de dominio DNS superior asignado a una partición de dominio o directorio. Se establece en un objeto crossRef y se usa, entre otras cosas, para la generación de referencias. Al buscar en un árbol de dominio completo, la búsqueda debe iniciarse en el Dns-Root objeto . Este atributo puede tener varios valores, en cuyo caso se generan varias referencias.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| Ldap-Display-Name | dnsRoot                                     |
| Size              | \-                                          |
| Actualizar privilegios  | El sistema establece este valor.            |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| System-Id-Guid    | bf967959-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------|
| Id. de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Es de un solo valor       | Falso                                      |
| Está indexado             | Verdadero                                       |
| En el catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------|
| Id. de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Es de un solo valor       | Falso                                      |
| Está indexado             | Verdadero                                       |
| En el catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|--------------------------------------------|
| Id. de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Es de un solo valor       | Falso                                      |
| Está indexado             | Verdadero                                       |
| En el catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------|
| Id. de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Es de un solo valor       | Falso                                      |
| Está indexado             | Verdadero                                       |
| En el catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------|
| Id. de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Es de un solo valor       | Falso                                      |
| Está indexado             | Verdadero                                       |
| En el catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------|
| Id. de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Es de un solo valor       | Falso                                      |
| Está indexado             | Verdadero                                       |
| En el catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------|
| Id. de vínculo                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | Falso                                      |
| Es de un solo valor       | Falso                                      |
| Está indexado             | Verdadero                                       |
| En el catálogo global      | Falso                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> |



 

 





