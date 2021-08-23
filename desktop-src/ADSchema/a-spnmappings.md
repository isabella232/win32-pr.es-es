---
title: SPN-Mappings atributo
description: Este atributo de varios valores contiene una lista de nombres de entidad de seguridad de servicio (SPN) para mostrar la equivalencia de los tipos de SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- SPN-Mappings esquema de AD de atributo
- Esquema de AD del atributo sPNMappings
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 451f8d3f98984f725915410e964e39a66905f29c1ccbcf9156b55d7ba51d3e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960054"
---
# <a name="spn-mappings-attribute"></a>SPN-Mappings atributo

Este atributo de varios valores contiene una lista de nombres de entidad de seguridad de servicio (SPN) para mostrar la equivalencia de los tipos de SPN. El SPN es el nombre que usa un cliente para identificar de forma única una instancia de un servicio. Si instala varias instancias de un servicio en equipos a lo largo de un bosque, cada instancia debe tener su propio SPN. Una instancia de servicio determinada puede tener varios SPN si hay varios nombres que los clientes pueden usar para la autenticación. Por ejemplo, "ldap/..." Los SPN se podrían asignar para que sean equivalentes a "host/..." Spn.



| Entrada | Value |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| Ldap-Display-Name | sPNMappings                                                                                                        |
| Size              | \-                                                                                                                 |
| Actualizar privilegios  | Este valor se establece durante la instalación del producto. El administrador del sistema puede modificarlo más adelante. |
| Frecuencia de actualización  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| System-Id-Guid    | 2ab0e76c-7041-11d2-9905-0000f87a57d4                                                                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                        |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Es de un solo valor       | Falso                                            |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Es de un solo valor       | Falso                                            |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Es de un solo valor       | Falso                                            |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Es de un solo valor       | Falso                                            |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Es de un solo valor       | Falso                                            |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Id. de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Es de un solo valor       | Falso                                            |
| Está indexado             | Falso                                            |
| En el catálogo global      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



 

 





