---
title: atributo MS-DS-site-Affinity
description: El atributo MS-DS-site-Affinity es utilizado por el administrador de cuentas de seguridad para la expansión de grupos durante la evaluación de tokens.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de afinidad de MS-DS-site
- msDS-site-Affinity atributo AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd3ed17b07c73d9e7a6a2d93d93463e1dea40fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906184"
---
# <a name="ms-ds-site-affinity-attribute"></a>atributo MS-DS-site-Affinity

El atributo **MS-DS-site-Affinity** es utilizado por el administrador de cuentas de seguridad para la expansión de grupos durante la evaluación de tokens.



| Entrada | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| CN                | Afinidad de MS-DS-site                                                                     |
| Nombre para mostrar de LDAP | msDS-site-Affinity                                                                      |
| Tamaño              | BLOB binario de varios valores, donde cada valor es sizeof (GUID) + sizeof (entero grande \_ ). |
| Actualizar privilegio  | \-                                                                                      |
| Frecuencia de actualización  | De forma predeterminada, una vez cada tres meses.                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.1443                                                                 |
| System-ID-GUID    | c17c5602-bcb7-46f0-9656-6370ca884b72                                                    |
| Sintaxis            | [**Object(Replica-Link)**](s-object-replica-link.md)                                   |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | False                             |
| Está indexado             | True                              |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | False                             |
| Está indexado             | True                              |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | False                             |
| Está indexado             | True                              |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | False                             |
| Está indexado             | True                              |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | False                             |
| Está indexado             | True                              |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



 

 





