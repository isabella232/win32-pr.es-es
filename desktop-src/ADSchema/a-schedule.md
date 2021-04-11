---
title: Atributo de programación
description: Un BLOB en programación tal y como se define en el servicio de trabajo de Windows NT. Usada por la replicación.
ms.assetid: 5eb6409d-3fb5-4368-8b7f-ce19567b7260
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de programación
- Esquema de AD de atributos de programación
topic_type:
- apiref
api_name:
- Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abf53e86f77ecffc872d8b007e32b1f964ae244e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151576"
---
# <a name="schedule-attribute"></a>Atributo de programación

Un BLOB en programación tal y como se define en el servicio de trabajo de Windows NT. Usada por la replicación.



| Entrada | Value |
|-------------------|-------------------------------------------------------|
| CN                | Programación                                              |
| Nombre para mostrar de LDAP | schedule                                              |
| Tamaño              | \-                                                    |
| Actualizar privilegio  | \-                                                    |
| Frecuencia de actualización  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.211                                |
| System-ID-GUID    | dd712224-10e4-11d0-a05f-00aa006c33ed                  |
| Sintaxis            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                             |
| Está indexado             | False                                                                                                                                                                                                                                                                            |
| En el catálogo global      | False                                                                                                                                                                                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> [**NTFRS: suscriptor**](c-ntfrssubscriber.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                             |
| Está indexado             | False                                                                                                                                                                                                                                                                            |
| En el catálogo global      | False                                                                                                                                                                                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> [**NTFRS: suscriptor**](c-ntfrssubscriber.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                            |
| MAPI-Id                | \-                                                                                                                                                            |
| System-Only            | False                                                                                                                                                         |
| Tiene un único valor       | True                                                                                                                                                          |
| Está indexado             | False                                                                                                                                                         |
| En el catálogo global      | False                                                                                                                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                  |
| Range-Lower            | \-                                                                                                                                                            |
| Range-Upper            | \-                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                                                    |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                             |
| Está indexado             | False                                                                                                                                                                                                                                                                            |
| En el catálogo global      | False                                                                                                                                                                                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> [**NTFRS: suscriptor**](c-ntfrssubscriber.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                             |
| Está indexado             | False                                                                                                                                                                                                                                                                            |
| En el catálogo global      | False                                                                                                                                                                                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> [**NTFRS: suscriptor**](c-ntfrssubscriber.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                             |
| Está indexado             | False                                                                                                                                                                                                                                                                            |
| En el catálogo global      | False                                                                                                                                                                                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> [**NTFRS: suscriptor**](c-ntfrssubscriber.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Tiene un único valor       | True                                                                                                                                                                                                                                                                             |
| Está indexado             | False                                                                                                                                                                                                                                                                            |
| En el catálogo global      | False                                                                                                                                                                                                                                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-set**](c-ntfrsreplicaset.md)<br/> [**NTFRS: suscriptor**](c-ntfrssubscriber.md)<br/> [**Sitio-vínculo**](c-sitelink.md)<br/> |



 

 





