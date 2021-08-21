---
title: Atributo Netboot-GUID
description: Arranque sin disco GUID de un equipo. Corresponde a la dirección MAC de la tarjeta de red del equipo.
ms.assetid: 60ce0482-79a3-499a-9607-f1f496e297d0
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Netboot-GUID
- Esquema de AD del atributo netbootGUID
topic_type:
- apiref
api_name:
- Netboot-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40eb39a4dcde5111e67734b7a0cc8cf3518f3fa8b03fa587744fb7fdec3a2c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118176289"
---
# <a name="netboot-guid-attribute"></a>Atributo Netboot-GUID

Arranque sin disco: GUID de un equipo. Corresponde a la dirección MAC de la tarjeta de red del equipo.



| Entrada | Valor |
|-------------------|-------------------------------------------------------|
| CN                | Netboot-GUID                                          |
| Ldap-Display-Name | netbootGUID                                           |
| Size              | \-                                                    |
| Privilegio actualizar  | El sistema establece este valor.                      |
| Frecuencia de actualización  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.359                                |
| System-Id-Guid    | 3e978921-8c01-11d0-afda-00c04fd930c9                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-------------------------------------------|
| Id. de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Falso                                     |
| Es de un solo valor       | True                                      |
| Está indexado             | True                                      |
| En el catálogo global      | Verdadero                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                              |
| Range-Lower            | 16                                        |
| Range-Upper            | 16                                        |
| Search-Flags           | 0x00000001                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------|
| Id. de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Falso                                     |
| Es de un solo valor       | Verdadero                                      |
| Está indexado             | Verdadero                                      |
| En el catálogo global      | Verdadero                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                              |
| Range-Lower            | 16                                        |
| Range-Upper            | 16                                        |
| Search-Flags           | 0x00000001                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------|
| Id. de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Falso                                     |
| Es de un solo valor       | Verdadero                                      |
| Está indexado             | True                                      |
| En el catálogo global      | True                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                              |
| Range-Lower            | 16                                        |
| Range-Upper            | 16                                        |
| Search-Flags           | 0x00000001                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------|
| Id. de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Falso                                     |
| Es de un solo valor       | True                                      |
| Está indexado             | Verdadero                                      |
| En el catálogo global      | True                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                              |
| Range-Lower            | 16                                        |
| Range-Upper            | 16                                        |
| Search-Flags           | 0x00000001                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------|
| Id. de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Falso                                     |
| Es de un solo valor       | Verdadero                                      |
| Está indexado             | True                                      |
| En el catálogo global      | True                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                              |
| Range-Lower            | 16                                        |
| Range-Upper            | 16                                        |
| Search-Flags           | 0x00000001                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------|
| Id. de vínculo                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Falso                                     |
| Es de un solo valor       | Verdadero                                      |
| Está indexado             | Verdadero                                      |
| En el catálogo global      | Verdadero                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                              |
| Range-Lower            | 16                                        |
| Range-Upper            | 16                                        |
| Search-Flags           | 0x00000001                                |
| System-Flags           | 0x00000010                                |
| Clases usadas en        | [**Computer**](c-computer.md)<br/> |



 

 





