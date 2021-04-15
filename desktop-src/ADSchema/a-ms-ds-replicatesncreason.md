---
title: Atributo MS-DS-Replications-NC-Reason
description: Atributo del objeto ntdsConnection que indica por qué (o si) el KCC muestra que la conexión es útil en la topología de replicación. Tiene varios valores y tiene DistName + sintaxis binaria, donde la parte binaria es un campo de bits de tamaño int.
ms.assetid: ba66e346-d288-4c0b-b41e-599c3f8e8405
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo MS-DS-Replications-NC-Reason
- Esquema de AD del atributo mS-DS-ReplicatesNCReason
topic_type:
- apiref
api_name:
- MS-DS-Replicates-NC-Reason
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a45c587ef82773b5e7fd310e8e8591f18ad27ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104422653"
---
# <a name="ms-ds-replicates-nc-reason-attribute"></a>Atributo MS-DS-Replications-NC-Reason

Atributo del objeto ntdsConnection que indica por qué (o si) el KCC muestra que la conexión es útil en la topología de replicación. Tiene varios valores y tiene DistName + sintaxis binaria, donde la parte binaria es un campo de bits de tamaño int.



| Entrada | Value |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-DS-Replications-NC-motivo                                                                                                                 |
| Nombre para mostrar de LDAP | mS-DS-ReplicatesNCReason                                                                                                                   |
| Tamaño              | Valor de la parte binaria: 0 = sin \_ motivo, 1 = topología de GC \_ , 2 = topología en anillo \_ , 4 = minimizar la \_ \_ topología de saltos, 8 = topología de servidores obsoletos \_ \_ . |
| Actualizar privilegio  | El sistema establece este valor.                                                                                                           |
| Frecuencia de actualización  | Puede cambiar en respuesta a los cambios en la topología de red.                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1408                                                                                                                    |
| System-ID-GUID    | 0ea12b84-08b3-11d3-91bc-0000f87a57d4                                                                                                       |
| Sintaxis            | [**Object(DN-Binary)**](s-object-dn-binary.md)                                                                                            |



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
|------------------------|--------------------------------------------------------|
| Identificador de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Tiene un único valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Identificador de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Tiene un único valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Identificador de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Tiene un único valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Identificador de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Tiene un único valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Identificador de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Tiene un único valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Identificador de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Tiene un único valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------|
| Identificador de vínculo                | \-                                                     |
| MAPI-Id                | \-                                                     |
| System-Only            | False                                                  |
| Tiene un único valor       | False                                                  |
| Está indexado             | False                                                  |
| En el catálogo global      | False                                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                           |
| Range-Lower            | \-                                                     |
| Range-Upper            | \-                                                     |
| Search-Flags           | 0x00000000                                             |
| System-Flags           | 0x00000010                                             |
| Clases usadas en        | [**NTDS-conexión**](c-ntdsconnection.md)<br/> |



 

 





