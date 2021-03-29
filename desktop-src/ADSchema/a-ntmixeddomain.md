---
title: 'NT: atributo de dominio mixto'
description: Indica que el dominio está en modo nativo o mixto. Este atributo se encuentra en el objeto domainDNS (Head) del dominio.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- NT-Mixed-esquema de AD de atributos de dominio
- nTMixedDomain esquema de AD de atributos
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658789"
---
# <a name="nt-mixed-domain-attribute"></a>NT: atributo de dominio mixto

Indica que el dominio está en modo nativo o mixto. Este atributo se encuentra en el objeto domainDNS (Head) del dominio.



| Entrada | Value |
|-------------------|---------------------------------------|
| CN                | NT-Mixed-Domain                       |
| Nombre para mostrar de LDAP | nTMixedDomain                         |
| Tamaño              | 4 bytes. Modo mixto 1, modo nativo 0. |
| Actualizar privilegio  | \-                                    |
| Frecuencia de actualización  | \-                                    |
| Attribute-Id      | 1.2.840.113556.1.4.357                |
| System-ID-GUID    | 3e97891f-8c01-11d0-afda-00c04fd930c9  |
| Sintaxis            | [**Enumeración**](s-enumeration.md)  |



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
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | False                                        |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**Sam-dominio**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Tiene un único valor       | True                                                                                    |
| Está indexado             | False                                                                                   |
| En el catálogo global      | False                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Tiene un único valor       | True                                                                                    |
| Está indexado             | False                                                                                   |
| En el catálogo global      | False                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Tiene un único valor       | True                                                                                    |
| Está indexado             | False                                                                                   |
| En el catálogo global      | False                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Tiene un único valor       | True                                                                                    |
| Está indexado             | False                                                                                   |
| En el catálogo global      | False                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                      |
| MAPI-Id                | \-                                                                                      |
| System-Only            | False                                                                                   |
| Tiene un único valor       | True                                                                                    |
| Está indexado             | False                                                                                   |
| En el catálogo global      | False                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000010                                                                              |
| Clases usadas en        | [**Referencia cruzada**](c-crossref.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> |



 

 





