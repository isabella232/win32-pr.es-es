---
title: Tombstone-Lifetime atributo
description: Número de días antes de que se quite un objeto eliminado de los servicios de directorio.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Tombstone-Lifetime esquema de AD del atributo
- tombstoneLifetime attribute AD Schema
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96d440b82f488e7968f787ae52d9f431350bee6050bd50b385f5751f51e76a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644955"
---
# <a name="tombstone-lifetime-attribute"></a>Tombstone-Lifetime atributo

Número de días antes de que se quite un objeto eliminado de los servicios de directorio. Esto ayuda a quitar objetos de servidores replicados e impedir que las restauraciones repliquen un objeto eliminado. Este valor está en el objeto Servicio de directorio de la NIC de configuración.



| Entrada | Valor |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| Ldap-Display-Name | tombstoneLifetime                                         |
| Size              | 4 bytes. El valor predeterminado es 60 días cuando no se introduce ningún valor. |
| Privilegio actualizar  | \-                                                        |
| Frecuencia de actualización  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| System-Id-Guid    | 16c3a860-1273-11d0-a060-00aa006c33ed                      |
| Syntax            | [**Enumeración**](s-enumeration.md)                      |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Es de un solo valor       | Verdadero                                             |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Es de un solo valor       | Verdadero                                             |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Es de un solo valor       | Verdadero                                             |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Es de un solo valor       | Verdadero                                             |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Es de un solo valor       | Verdadero                                             |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Es de un solo valor       | Verdadero                                             |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Es de un solo valor       | Verdadero                                             |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



 

 





