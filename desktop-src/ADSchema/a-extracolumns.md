---
title: Extra-Columns atributo
description: Se trata de un atributo de varios valores cuyos valores constan de una tupla 5 (nombre de atributo), (título de columna), (visibilidad predeterminada (0,1)), (ancho de columna ( \ 8211;1 para el ancho automático)), 0 (reservado para uso futuro debe ser cero).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Extra-Columns esquema de AD del atributo
- Esquema de AD del atributo extraColumns
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6314a18ecac01a306c72d5879d191c5a744c20171495a3d57192078202d129f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177187"
---
# <a name="extra-columns-attribute"></a>Extra-Columns atributo

Se trata de un atributo de varios valores cuyos valores constan de una tupla de 5: (nombre de atributo), (título de columna), (visibilidad predeterminada (0,1)), (ancho de columna ( 1 para ancho automático)), 0 (reservado para uso futuro debe ser cero). La consola usuarios y equipos de AD usa este valor.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Extra-Columns                                                                                                                                                        |
| Ldap-Display-Name | extraColumns                                                                                                                                                         |
| Size              | Cada valor sería el tamaño de la cadena de las 5 tuplas anteriores. De forma predeterminada, habrá 22 valores en el objeto default-Display en el contenedor DisplaySpecifier. |
| Privilegio actualizar  | Administrador de dominio                                                                                                                                                 |
| Frecuencia de actualización  | Esto solo se actualizará si un servicio como Exchange está instalado.                                                                                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1687                                                                                                                                              |
| System-Id-Guid    | d24e2846-1dd9-4bcf-99d7-a6227cc86da7                                                                                                                                 |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------|
| Id. de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Es de un solo valor       | Falso                                                      |
| Está indexado             | Falso                                                      |
| En el catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------|
| Id. de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Es de un solo valor       | Falso                                                      |
| Está indexado             | Falso                                                      |
| En el catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| Id. de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Es de un solo valor       | Falso                                                      |
| Está indexado             | Falso                                                      |
| En el catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------|
| Id. de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Es de un solo valor       | Falso                                                      |
| Está indexado             | Falso                                                      |
| En el catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------|
| Id. de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| Es de un solo valor       | Falso                                                      |
| Está indexado             | Falso                                                      |
| En el catálogo global      | Falso                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



 

 





