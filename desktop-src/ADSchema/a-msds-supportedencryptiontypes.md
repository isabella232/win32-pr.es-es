---
title: atributo MS-DS-Supported-Encryption-Types
description: Los algoritmos de cifrado compatibles con cuentas de usuario, equipo o confianza. Tenga en cuenta que el KDC usa esta información durante la generación de un vale de servicio para esta cuenta.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- MS-DS-Supported-Encryption-Types atributo AD Schema
- Esquema de AD de atributo msDS-SupportedEncryptionTypes
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105659104"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>atributo MS-DS-Supported-Encryption-Types

Los algoritmos de cifrado compatibles con cuentas de usuario, equipo o confianza.

> [!Note]  
> El KDC usa esta información durante la generación de un vale de servicio para esta cuenta. Los servicios y equipos pueden actualizar automáticamente este atributo en sus cuentas respectivas en Active Directory y, por tanto, necesitan tener acceso de escritura a este atributo.

 



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-DS-compatible-tipos de cifrado     |
| Nombre para mostrar de LDAP | msDS-SupportedEncryptionTypes        |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-ID-GUID    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | False                                                                                  |
| Tiene un único valor       | True                                                                                   |
| Está indexado             | False                                                                                  |
| En el catálogo global      | False                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | False                                                                                  |
| Tiene un único valor       | True                                                                                   |
| Está indexado             | False                                                                                  |
| En el catálogo global      | False                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | False                                                                                  |
| Tiene un único valor       | True                                                                                   |
| Está indexado             | False                                                                                  |
| En el catálogo global      | False                                                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> [**Usuario**](c-user.md)<br/> |



 

 





