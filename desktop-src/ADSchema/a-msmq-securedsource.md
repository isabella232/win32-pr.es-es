---
title: Atributo MSMQ-Secured-Source
description: Esto forma parte de un objeto MSMQ, se establece mediante una llamada API a MQCreateQueue o MQSetProperties. Controla si MSMQ acepta mensajes solo de un origen protegido (por ejemplo, https) para esta cola.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MSMQ-Secured-Source
- MSMQ-SecuredSource esquema de AD de atributo
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23785fd626debe61981185561b3b1ea243d93ff870fc2e025777488e1d898c16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762755"
---
# <a name="msmq-secured-source-attribute"></a>Atributo MSMQ-Secured-Source

Esto forma parte de un objeto MSMQ, se establece mediante una llamada API a MQCreateQueue o MQSetProperties. Controla si MSMQ acepta mensajes solo de un origen protegido (por ejemplo, https) para esta cola.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Origen protegido por MSMQ                  |
| Ldap-Display-Name | MSMQ-SecuredSource                   |
| Size              | 4 bytes                              |
| Actualizar privilegios  | Propietario de la cola.                     |
| Frecuencia de actualización  | Cuando se crea una cola.             |
| Attribute-Id      | 1.2.840.113556.1.4.1713              |
| System-Id-Guid    | 8bf0221b-7a06-4d63-91f0-1499941813d3 |
| Syntax            | [**Booleana**](s-boolean.md)         |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Verdadero                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Verdadero                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Verdadero                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Verdadero                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------|
| Id. de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Es de un solo valor       | Verdadero                                         |
| Está indexado             | Falso                                        |
| En el catálogo global      | Verdadero                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-Queue**](c-msmqqueue.md)<br/> |



 

 





