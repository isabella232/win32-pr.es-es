---
title: Repl-Interval atributo
description: Atributo de Site-Link que define el intervalo, en minutos, entre los ciclos de replicación entre los sitios de la lista de sitios.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Repl-Interval esquema de AD de atributo
- Esquema de AD del atributo replInterval
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5cd02d3458684f6d70cff84435c7809fcd4c912befd65373a264f961cefd72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837445"
---
# <a name="repl-interval-attribute"></a>Repl-Interval atributo

Atributo de Site-Link que define el intervalo, en minutos, entre los ciclos de replicación entre los sitios de la lista de sitios. Debe ser un múltiplo de 15 minutos (la granularidad de la replicación de DS entre sitios), un mínimo de 15 minutos y un máximo de 10 080 minutos (una semana).



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | Repl-Interval                                  |
| Ldap-Display-Name | replInterval                                   |
| Size              | 4 bytes                                        |
| Actualizar privilegios  | Administrador de empresa                       |
| Frecuencia de actualización  | Cuando es necesario cambiar el intervalo de replicación. |
| Attribute-Id      | 1.2.840.113556.1.4.1336                        |
| System-Id-Guid    | 45ba9d1a-56fa-11d2-90d0-00c04fd91ab1           |
| Syntax            | [**Enumeración**](s-enumeration.md)           |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                       |
| Está indexado             | Falso                                                                                                      |
| En el catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                       |
| Está indexado             | Falso                                                                                                      |
| En el catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                       |
| Está indexado             | Falso                                                                                                      |
| En el catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                       |
| Está indexado             | Falso                                                                                                      |
| En el catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                       |
| Está indexado             | Falso                                                                                                      |
| En el catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                       |
| Está indexado             | Falso                                                                                                      |
| En el catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                       |
| Está indexado             | Falso                                                                                                      |
| En el catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Clases usadas en        | [**Transporte entre sitios**](c-intersitetransport.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



 

 





