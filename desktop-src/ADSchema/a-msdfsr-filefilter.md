---
title: atributo MS-DFSR-FileFilter
description: Contiene la cadena de filtro que se utiliza para filtrar los archivos.
ms.assetid: e9c57328-e7c0-4149-aa1d-64603844e001
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DFSR-FileFilter
- msDFSR-FileFilter Attribute AD Schema
topic_type:
- apiref
api_name:
- ms-DFSR-FileFilter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 597a5e722cd38213d0c668c0afdfc6094288ae80
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658913"
---
# <a name="ms-dfsr-filefilter-attribute"></a>atributo MS-DFSR-FileFilter

Contiene la cadena de filtro que se utiliza para filtrar los archivos.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | MS-DFSR-FileFilter                          |
| Nombre para mostrar de LDAP | msDFSR-FileFilter                           |
| Tamaño              | \-                                          |
| Actualizar privilegio  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.12                  |
| System-ID-GUID    | d68270ac-a5dc-4841-a6ac-cd68be38c181        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | False                                                        |
| En el catálogo global      | False                                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 32767                                                        |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000000                                                   |
| Clases usadas en        | [**MS-DFSR-ContentSet**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | False                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                  |
| Está indexado             | False                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                          |
| Range-Lower            | 0                                                                                                                                     |
| Range-Upper            | 32767                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Clases usadas en        | [**MS-DFSR-grupo**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-ContentSet**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | False                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                  |
| Está indexado             | False                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                          |
| Range-Lower            | 0                                                                                                                                     |
| Range-Upper            | 32767                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Clases usadas en        | [**MS-DFSR-grupo**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-ContentSet**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | False                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                  |
| Está indexado             | False                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                          |
| Range-Lower            | 0                                                                                                                                     |
| Range-Upper            | 32767                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| Clases usadas en        | [**MS-DFSR-grupo**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-ContentSet**](c-msdfsr-contentset.md)<br/> |



## <a name="remarks"></a>Observaciones

El atributo **MS-DFSR-FileFilter** forma parte de la compatibilidad con el servicio de replicación de sistema de archivos distribuido (DFS).

 

 





