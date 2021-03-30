---
title: Extra-Columns atributo)
description: Se trata de un atributo multivalor cuyos valores se componen de una tupla de 5 (nombre de atributo), (título de columna), (visibilidad predeterminada (0, 1)), (el ancho de columna (\ 8211; 1 para el ancho automático), 0 (reservado para uso futuro debe ser cero).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Extra-Columns
- atributo de extracolumns esquema de AD
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804435"
---
# <a name="extra-columns-attribute"></a>Extra-Columns atributo)

Se trata de un atributo multivalor cuyos valores se componen de una tupla 5: (nombre de atributo), (título de columna), (visibilidad predeterminada (0, 1)), (ancho de columna (1 para ancho automático), 0 (reservado para uso futuro debe ser cero). La consola usuarios y equipos de AD usa este valor.



| Entrada | Value |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Extra-Columns                                                                                                                                                        |
| Nombre para mostrar de LDAP | extracolumns                                                                                                                                                         |
| Tamaño              | Cada valor sería el tamaño de la cadena de la tupla 5 anterior. De forma predeterminada, habrá 22 valores en el objeto de visualización predeterminado en el contenedor DisplaySpecifier. |
| Actualizar privilegio  | Administrador de dominio                                                                                                                                                 |
| Frecuencia de actualización  | Solo se actualizará si se ha instalado un servicio como Exchange.                                                                                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1687                                                                                                                                              |
| System-ID-GUID    | d24e2846-1dd9-4bcf-99d7-a6227cc86da7                                                                                                                                 |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------|
| Identificador de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Tiene un único valor       | False                                                      |
| Está indexado             | False                                                      |
| En el catálogo global      | False                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------|
| Identificador de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Tiene un único valor       | False                                                      |
| Está indexado             | False                                                      |
| En el catálogo global      | False                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------|
| Identificador de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Tiene un único valor       | False                                                      |
| Está indexado             | False                                                      |
| En el catálogo global      | False                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------|
| Identificador de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Tiene un único valor       | False                                                      |
| Está indexado             | False                                                      |
| En el catálogo global      | False                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------|
| Identificador de vínculo                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Tiene un único valor       | False                                                      |
| Está indexado             | False                                                      |
| En el catálogo global      | False                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Clases usadas en        | [**Display-Specifier**](c-displayspecifier.md)<br/> |



 

 





