---
title: Atributo ms-TAPI-Protocol-Id
description: Este atributo indica el tipo de conferencia TAPI.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-TAPI-Protocol-Id
- Esquema de AD del atributo msTAPI-ProtocolId
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fb09579ae7c97c9a44140cf634b9fab42f257401fb00091ac74209b0a4908b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066185"
---
# <a name="ms-tapi-protocol-id-attribute"></a>Atributo ms-TAPI-Protocol-Id

Este atributo indica el tipo de conferencia TAPI. Este atributo se usa para determinar cómo se interpretará el blob binario en el atributo [**ms-TAPI-Conference-Blob.**](a-mstapi-conferenceblob.md) Este atributo es una cadena arbitraria, normalmente de menos de 100 caracteres de longitud.



| Entrada | Value |
|-------------------|------------------------------------------------------------|
| CN                | ms-TAPI-Protocol-Id                                        |
| Ldap-Display-Name | msTAPI-ProtocolId                                          |
| Size              | \-                                                         |
| Actualizar privilegios  | No se requieren privilegios especiales.                            |
| Frecuencia de actualización  | Establezca una vez en el momento de crear el Rt-Conference objeto . |
| Attribute-Id      | 1.2.840.113556.1.4.1699                                    |
| System-Id-Guid    | 89c1ebcf-7a5f-41fd-99ca-c900b32299ab                       |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Es de un solo valor       | Verdadero                                                              |
| Está indexado             | Falso                                                             |
| En el catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Es de un solo valor       | Verdadero                                                              |
| Está indexado             | Falso                                                             |
| En el catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Es de un solo valor       | Verdadero                                                              |
| Está indexado             | Falso                                                             |
| En el catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Es de un solo valor       | Verdadero                                                              |
| Está indexado             | Falso                                                             |
| En el catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Es de un solo valor       | Verdadero                                                              |
| Está indexado             | Falso                                                             |
| En el catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



 

 





