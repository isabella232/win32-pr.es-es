---
title: Atributo NT-Mixed-Domain
description: Indica que el dominio está en modo nativo o en modo mixto. Este atributo se encuentra en el objeto domainDNS (head) del dominio.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo NT-Mixed-Domain
- Esquema de AD del atributo nTMixedDomain
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39148883e2b5d57157c334854ab7ebdfa61b69ac61d7a0100fc8470b741909c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703035"
---
# <a name="nt-mixed-domain-attribute"></a>Atributo NT-Mixed-Domain

Indica que el dominio está en modo nativo o en modo mixto. Este atributo se encuentra en el objeto domainDNS (head) del dominio.



| Entrada | Valor |
|-------------------|---------------------------------------|
| CN                | NT-Mixed-Domain                       |
| Ldap-Display-Name | nTMixedDomain                         |
| Size              | 4 bytes. Modo mixto 1, modo nativo 0. |
| Actualizar privilegios  | \-                                    |
| Frecuencia de actualización  | \-                                    |
| Attribute-Id      | 1.2.840.113556.1.4.357                |
| System-Id-Guid    | 3e97891f-8c01-11d0-afda-00c04fd930c9  |
| Syntax            | [**Enumeración**](s-enumeration.md)  |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| Es de un solo valor       | Verdadero                                                                                    |
| Está indexado             | Falso                                                                                   |
| En el catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| Es de un solo valor       | Verdadero                                                                                    |
| Está indexado             | Falso                                                                                   |
| En el catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| Es de un solo valor       | Verdadero                                                                                    |
| Está indexado             | Falso                                                                                   |
| En el catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| Es de un solo valor       | Verdadero                                                                                    |
| Está indexado             | Falso                                                                                   |
| En el catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | Falso                                                                                   |
| Es de un solo valor       | Verdadero                                                                                    |
| Está indexado             | Falso                                                                                   |
| En el catálogo global      | Falso                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> |



 

 





