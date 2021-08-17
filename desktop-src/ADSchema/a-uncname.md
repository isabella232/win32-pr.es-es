---
title: UNC-Name atributo
description: Nombre de la convención de nomenclatura universal para impresoras y volúmenes compartidos.
ms.assetid: 967fd0dc-10af-4482-bc2c-1d1dc13dee39
ms.tgt_platform: multiple
keywords:
- UNC-Name esquema de AD del atributo
- Esquema de AD del atributo uNCName
topic_type:
- apiref
api_name:
- UNC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6227aaed6ac68c04de1ce8425281674117e11dcb33f8c50db696cff0ea8d8ae8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681601"
---
# <a name="unc-name-attribute"></a>UNC-Name atributo

Nombre de la convención de nomenclatura universal para impresoras y volúmenes compartidos.



| Entrada | Valor |
|-------------------|-----------------------------------------------|
| CN                | UNC-Name                                      |
| Ldap-Display-Name | uNCName                                       |
| Size              | \-                                            |
| Privilegio actualizar  | Administrador de dominio                          |
| Frecuencia de actualización  | Cuando se crean nuevos volúmenes o colas de impresión. |
| Attribute-Id      | 1.2.840.113556.1.4.137                        |
| System-Id-Guid    | bf967a64-0de6-11d0-a285-00aa003049e2          |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)   |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                           |
| Clases usadas en        | [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                        |
| MAPI-Id                | \-                                                                                                                                                                                        |
| System-Only            | Falso                                                                                                                                                                                     |
| Es de un solo valor       | Verdadero                                                                                                                                                                                      |
| Está indexado             | Verdadero                                                                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                        |
| Search-Flags           | 0x00000001                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                |
| Clases usadas en        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**FT-Dfs**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**ms-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Cola de impresión**](c-printqueue.md)<br/> [**Volumen**](c-volume.md)<br/> |



 

 





