---
title: Trust-Partner atributo)
description: Nombre del dominio con el que existe una confianza.
ms.assetid: 0b7c8e78-614b-46dd-8616-40d75b461639
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Trust-Partner
- trustPartner esquema de AD de atributos
topic_type:
- apiref
api_name:
- Trust-Partner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201a89e178515b270302b4d8541af64a63ad6813
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151557"
---
# <a name="trust-partner-attribute"></a>Trust-Partner atributo)

Nombre del dominio con el que existe una confianza.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Trust-Partner                               |
| Nombre para mostrar de LDAP | trustPartner                                |
| Tamaño              | \-                                          |
| Actualizar privilegio  | El sistema establece este valor.            |
| Frecuencia de actualización  | Cuando se crea una nueva confianza.                |
| Attribute-Id      | 1.2.840.113556.1.4.133                      |
| System-ID-GUID    | bf967a5d-0de6-11d0-a285-00aa003049e2        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | True                                                 |
| En el catálogo global      | False                                                |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | True                                                 |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | True                                                 |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | True                                                 |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | True                                                 |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------|
| Identificador de vínculo                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Tiene un único valor       | True                                                 |
| Está indexado             | True                                                 |
| En el catálogo global      | True                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> |



 

 





