---
title: Atributo ms-DS-Logon-Time-Sync-Interval
description: Este atributo controla la granularidad, en días, con la que la hora de último inicio de sesión de un usuario o equipo, registrada en el atributo lastLogonTimestamp, se replica en todos los controladores de dominio de un dominio.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DS-Logon-Time-Sync-Interval
- Esquema de AD del atributo msDS-LogonTimeSyncInterval
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa27a1d6281eda7eea9f88a11c4ca6632422a1cfd9f0cb471aab513018c56150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118684639"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a>Atributo ms-DS-Logon-Time-Sync-Interval

Este atributo controla la granularidad, en días, con la que la hora de último inicio de sesión de un usuario o equipo, registrada en el atributo lastLogonTimestamp, se replica en todos los controladores de dominio de un dominio.



| Entrada | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Logon-Time-Sync-Interval                                                                             |
| Ldap-Display-Name | msDS-LogonTimeSyncInterval                                                                                 |
| Size              | 4 bytes                                                                                                    |
| Actualizar privilegios  | Administrador de dominio                                                                                       |
| Frecuencia de actualización  | En raras ocasiones, dado que se trata de una configuración de directiva, solo se actualiza cuando se desea un cambio en la directiva de todo el dominio. |
| Attribute-Id      | 1.2.840.113556.1.4.1784                                                                                    |
| System-Id-Guid    | ad7940f8-e43a-4a42-83bc-d688e59ea605                                                                       |
| Syntax            | [**Enumeración**](s-enumeration.md)                                                                       |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
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



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
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



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
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



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
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



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
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



 

 





