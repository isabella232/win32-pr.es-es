---
title: UNC-Name atributo)
description: Nombre de la Convención de nomenclatura universal para impresoras y volúmenes compartidos.
ms.assetid: 967fd0dc-10af-4482-bc2c-1d1dc13dee39
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de UNC-Name
- uNCName esquema de AD de atributos
topic_type:
- apiref
api_name:
- UNC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e06bc54ebb035a491e2d93a1c372e2d46fc43f76
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658724"
---
# <a name="unc-name-attribute"></a>UNC-Name atributo)

Nombre de la Convención de nomenclatura universal para impresoras y volúmenes compartidos.



| Entrada | Value |
|-------------------|-----------------------------------------------|
| CN                | UNC-Name                                      |
| Nombre para mostrar de LDAP | uNCName                                       |
| Tamaño              | \-                                            |
| Actualizar privilegio  | Administrador de dominio                          |
| Frecuencia de actualización  | Cuando se crean nuevos volúmenes o colas de impresión. |
| Attribute-Id      | 1.2.840.113556.1.4.137                        |
| System-ID-GUID    | bf967a64-0de6-11d0-a285-00aa003049e2          |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)   |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                   |
| System-Only            | False                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                           |
| Clases usadas en        | [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                        |
| MAPI-Id                | \-                                                                                                                                                                                        |
| System-Only            | False                                                                                                                                                                                     |
| Tiene un único valor       | True                                                                                                                                                                                      |
| Está indexado             | True                                                                                                                                                                                      |
| En el catálogo global      | True                                                                                                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                        |
| Search-Flags           | 0x00000001                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                |
| Clases usadas en        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                 |
| Está indexado             | True                                                                                                                                                                                                                                                                 |
| En el catálogo global      | True                                                                                                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



 

 





