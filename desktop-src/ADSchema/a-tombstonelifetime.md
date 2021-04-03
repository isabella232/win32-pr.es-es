---
title: Tombstone-Lifetime atributo)
description: El número de días antes de que se quite un objeto eliminado de los servicios de directorio.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Tombstone-Lifetime
- tombstoneLifetime (atributo) esquema de AD
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906097"
---
# <a name="tombstone-lifetime-attribute"></a>Tombstone-Lifetime atributo)

El número de días antes de que se quite un objeto eliminado de los servicios de directorio. Esto ayuda a quitar objetos de los servidores replicados y evitar que las restauraciones representen un objeto eliminado. Este valor se encuentra en el objeto de servicio de directorio en la NIC de configuración.



| Entrada | Value |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| Nombre para mostrar de LDAP | tombstoneLifetime                                         |
| Tamaño              | 4 bytes. El valor predeterminado es 60 días cuando no se especifica ningún valor. |
| Actualizar privilegio  | \-                                                        |
| Frecuencia de actualización  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| System-ID-GUID    | 16c3a860-1273-11d0-a060-00aa006c33ed                      |
| Sintaxis            | [**Enumeración**](s-enumeration.md)                      |



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
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



 

 





