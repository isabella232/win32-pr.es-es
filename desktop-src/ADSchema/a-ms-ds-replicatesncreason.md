---
title: Atributo MS-DS-Replicates-NC-Reason
description: Atributo del objeto ntdsConnection que indica por qué (o si) el KCC muestra que la conexión es útil en la topología de replicación. Tiene varios valores y tiene sintaxis DistName+Binary, donde la parte binaria es un campo de bits de tamaño int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Replicates-NC-Reason
- Esquema de AD del atributo mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681105fe24584afae275a8869ad04698ff7a70daa32832140a98865318672863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118686976"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>Atributo MS-DS-Replicates-NC-Reason

Atributo del objeto ntdsConnection que indica por qué (o si) el KCC muestra que la conexión es útil en la topología de replicación. Tiene varios valores y tiene sintaxis DistName+Binary, donde la parte binaria es un campo de bits de tamaño int.



| Entrada | Value |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-Replicates-NC-Reason                                                                                                                 |
| Ldap-Display-Name | mS-DS-ReplicatesNCReason                                                                                                                   |
| Size              | Valor de la parte binaria: 0 = NO \_ REASON,1 = GC \_ TOPOLOGY, 2 = RING \_ TOPOLOGY, 4 = MINIMIZE \_ HOPS \_ TOPOLOGY, 8 = STALE \_ SERVERS \_ TOPOLOGY. |
| Privilegio actualizar  | El sistema establece este valor.                                                                                                           |
| Frecuencia de actualización  | Puede cambiar en respuesta a los cambios en la topología de red.                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| System-Id-Guid    | 0ea12b84-08b3-11d3-91bc-0000f87a57d4                                                                                                       |
| Sintaxis            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                            |



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
|------------------------|--------------------------------------------------------|
| Id. de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Es de un solo valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Id. de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Es de un solo valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Id. de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Es de un solo valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Id. de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Es de un solo valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Id. de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Es de un solo valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Id. de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Es de un solo valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Id. de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Es de un solo valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-Connection**](c-ntdsconnection.md)<br/> |



 

 





