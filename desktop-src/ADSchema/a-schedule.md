---
title: Atributo Schedule
description: Blob de programación tal y como lo define el Windows servicio de trabajo nt. Usado por la replicación.
ms.assetid: 5eb6409d-3fb5-4368-8b7f-ce19567b7260
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de programación
- esquema de AD de atributo de programación
topic_type:
- apiref
api_name:
- Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b65ff20b9eaba0c8429f5fec164e44a3e4b842e82bfddcca61461f6832f55d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022223"
---
# <a name="schedule-attribute"></a>Atributo Schedule

Blob de programación tal y como lo define el Windows servicio de trabajo nt. Usado por la replicación.



| Entrada | Value |
|-------------------|-------------------------------------------------------|
| CN                | Programación                                              |
| Ldap-Display-Name | schedule                                              |
| Size              | \-                                                    |
| Privilegio actualizar  | \-                                                    |
| Frecuencia de actualización  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.211                                |
| System-Id-Guid    | dd712224-10e4-11d0-a05f-00aa006c33ed                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                             |
| Está indexado             | Falso                                                                                                                                                                                                                                                                            |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> [**NTDS-Site-Configuración**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                             |
| Está indexado             | Falso                                                                                                                                                                                                                                                                            |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> [**NTDS-Site-Configuración**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                            |
| MAPI-Id                | \-                                                                                                                                                            |
| System-Only            | Falso                                                                                                                                                         |
| Es de un solo valor       | Verdadero                                                                                                                                                          |
| Está indexado             | Falso                                                                                                                                                         |
| En el catálogo global      | Falso                                                                                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                  |
| Range-Lower            | \-                                                                                                                                                            |
| Range-Upper            | \-                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                                                    |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> [**NTDS-Site-Configuración**](c-ntdssitesettings.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                             |
| Está indexado             | Falso                                                                                                                                                                                                                                                                            |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> [**NTDS-Site-Configuración**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                             |
| Está indexado             | Falso                                                                                                                                                                                                                                                                            |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> [**NTDS-Site-Configuración**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                             |
| Está indexado             | Falso                                                                                                                                                                                                                                                                            |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> [**NTDS-Site-Configuración**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                             |
| Está indexado             | Falso                                                                                                                                                                                                                                                                            |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> [**NTDS-Site-Configuración**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Vínculo de sitio**](c-sitelink.md)<br/> |



 

 





