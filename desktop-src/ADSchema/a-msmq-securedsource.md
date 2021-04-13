---
title: Atributo MSMQ-Secure-Source
description: Esto forma parte de un objeto MSMQ, se establece mediante una llamada a la API a MQCreateQueue o MQSetProperties. Controla si MSMQ acepta mensajes solo de un origen protegido (por ejemplo, https) para esta cola.
ms.assetid: 780d164f-c7fa-4c65-b46e-3a67ead92163
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de origen de MSMQ-protegido
- Esquema de AD de atributo de MSMQ-SecuredSource
topic_type:
- apiref
api_name:
- MSMQ-Secured-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5dd005cedcd650aa0604a85e78a46d10f1e01b0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535974"
---
# <a name="msmq-secured-source-attribute"></a>Atributo MSMQ-Secure-Source

Esto forma parte de un objeto MSMQ, se establece mediante una llamada a la API a MQCreateQueue o MQSetProperties. Controla si MSMQ acepta mensajes solo de un origen protegido (por ejemplo, https) para esta cola.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Código fuente de MSMQ protegido                  |
| Nombre para mostrar de LDAP | MSMQ-SecuredSource                   |
| Tamaño              | 4 bytes                              |
| Actualizar privilegio  | Propietario de la cola.                     |
| Frecuencia de actualización  | Cuando se crea una cola.             |
| Attribute-Id      | 1.2.840.113556.1.4.1713              |
| System-ID-GUID    | 8bf0221b-7a06-4d63-91f0-1499941813d3 |
| Sintaxis            | [**Booleano**](s-boolean.md)         |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | True                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-cola**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | True                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-cola**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | True                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-cola**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | True                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-cola**](c-msmqqueue.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------|
| Identificador de vínculo                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Tiene un único valor       | True                                         |
| Está indexado             | False                                        |
| En el catálogo global      | True                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Clases usadas en        | [**MSMQ-cola**](c-msmqqueue.md)<br/> |



 

 





