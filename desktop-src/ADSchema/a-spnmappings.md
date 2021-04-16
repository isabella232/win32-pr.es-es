---
title: SPN-Mappings atributo)
description: Este atributo de varios valores contiene una lista de nombres de entidad de seguridad de servicio (SPN) para mostrar la equivalencia de los tipos de SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de SPN-Mappings
- sPNMappings esquema de AD de atributos
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536136"
---
# <a name="spn-mappings-attribute"></a>SPN-Mappings atributo)

Este atributo de varios valores contiene una lista de nombres de entidad de seguridad de servicio (SPN) para mostrar la equivalencia de los tipos de SPN. El SPN es el nombre que usa un cliente para identificar de forma única una instancia de un servicio. Si instala varias instancias de un servicio en equipos a lo largo de un bosque, cada instancia debe tener su propio SPN. Una instancia de servicio determinada puede tener varios SPN si hay varios nombres que los clientes pueden usar para la autenticación. Por ejemplo, "LDAP/..." Los SPN se pueden asignar de forma que sean equivalentes a "host/..." Carece.



| Entrada | Value |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| Nombre para mostrar de LDAP | sPNMappings                                                                                                        |
| Tamaño              | \-                                                                                                                 |
| Actualizar privilegio  | Este valor se establece durante la instalación del producto. Puede ser modificado por el administrador del sistema en un momento posterior. |
| Frecuencia de actualización  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| System-ID-GUID    | 2ab0e76c-7041-11d2-9905-0000f87a57d4                                                                               |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                                                        |



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
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Tiene un único valor       | False                                            |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Tiene un único valor       | False                                            |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Tiene un único valor       | False                                            |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Tiene un único valor       | False                                            |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Tiene un único valor       | False                                            |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | False                                            |
| Tiene un único valor       | False                                            |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



 

 





