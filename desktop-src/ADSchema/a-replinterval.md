---
title: Repl-Interval atributo)
description: El atributo de Site-Link objetos que define el intervalo, en minutos, entre los ciclos de replicación entre los sitios de la lista de sitios.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Repl-Interval
- replInterval esquema de AD de atributos
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151589"
---
# <a name="repl-interval-attribute"></a>Repl-Interval atributo)

El atributo de Site-Link objetos que define el intervalo, en minutos, entre los ciclos de replicación entre los sitios de la lista de sitios. Debe ser un múltiplo de 15 minutos (la granularidad de la replicación de DS entre sitios), un mínimo de 15 minutos y un máximo de 10.080 minutos (una semana).



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | Repl-Interval                                  |
| Nombre para mostrar de LDAP | replInterval                                   |
| Tamaño              | 4 bytes                                        |
| Actualizar privilegio  | Administrador de empresa                       |
| Frecuencia de actualización  | Cuándo es necesario cambiar el intervalo de replicación. |
| Attribute-Id      | 1.2.840.113556.1.4.1336                        |
| System-ID-GUID    | 45ba9d1a-56fa-11d2-90d0-00c04fd91ab1           |
| Sintaxis            | [**Enumeración**](s-enumeration.md)           |



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
|------------------------|------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Tiene un único valor       | True                                                                                                       |
| Está indexado             | False                                                                                                      |
| En el catálogo global      | False                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Tiene un único valor       | True                                                                                                       |
| Está indexado             | False                                                                                                      |
| En el catálogo global      | False                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Tiene un único valor       | True                                                                                                       |
| Está indexado             | False                                                                                                      |
| En el catálogo global      | False                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Tiene un único valor       | True                                                                                                       |
| Está indexado             | False                                                                                                      |
| En el catálogo global      | False                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Tiene un único valor       | True                                                                                                       |
| Está indexado             | False                                                                                                      |
| En el catálogo global      | False                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Tiene un único valor       | True                                                                                                       |
| Está indexado             | False                                                                                                      |
| En el catálogo global      | False                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Tiene un único valor       | True                                                                                                       |
| Está indexado             | False                                                                                                      |
| En el catálogo global      | False                                                                                                      |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



 

 





