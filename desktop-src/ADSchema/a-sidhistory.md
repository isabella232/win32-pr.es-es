---
title: SID-History atributo)
description: Contiene los SID anteriores usados para el objeto si el objeto se ha despasado de otro dominio.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de SID-History
- sIDHistory atributo AD Schema
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16474a6463fc99e7ed2c1d2b1a2cdbf6ea9b6614
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493691"
---
# <a name="sid-history-attribute"></a>SID-History atributo)

Contiene los SID anteriores usados para el objeto si el objeto se ha despasado de otro dominio. Cada vez que un objeto se mueve de un dominio a otro, se crea un nuevo SID y ese nuevo SID se convierte en el objectSID. El SID anterior se agrega a la propiedad sIDHistory.



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | SID-History                                    |
| Nombre para mostrar de LDAP | Correspondientes                                     |
| Tamaño              | \-                                             |
| Actualizar privilegio  | El sistema establece este valor.               |
| Frecuencia de actualización  | Cada vez que el objeto se mueve a un nuevo dominio. |
| Attribute-Id      | 1.2.840.113556.1.4.609                         |
| System-ID-GUID    | 17eb4278-d167-11d0-b002-0000f80367c1           |
| Sintaxis            | [**Cadena (SID)**](s-string-sid.md)            |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | True                                                         |
| Tiene un único valor       | False                                                        |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | False                                                        |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





