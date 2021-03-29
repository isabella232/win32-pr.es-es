---
title: Atributo App-Schema-version
description: Este atributo almacena la versión del esquema del almacén de clases. Se usa para proporcionar el comportamiento correcto a través de los cambios de esquema.
ms.assetid: e8c2ab2b-1b7f-4d4f-b9ea-4116a8e30277
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de versión de esquema de aplicación
- appSchemaVersion esquema de AD de atributos
topic_type:
- apiref
api_name:
- App-Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09265299a676ef6b9d319153c7efdbe3929ee883
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658671"
---
# <a name="app-schema-version-attribute"></a>Atributo App-Schema-version

Este atributo almacena la versión del esquema del almacén de clases. Se usa para proporcionar el comportamiento correcto a través de los cambios de esquema.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Versión del esquema de la aplicación                   |
| Nombre para mostrar de LDAP | appSchemaVersion                     |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.848               |
| System-ID-GUID    | 96a7dd65-9118-11d1-aebc-0000f80367c1 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|------------------------------------------------|
| Identificador de vínculo                | \-                                             |
| MAPI-Id                | \-                                             |
| System-Only            | False                                          |
| Tiene un único valor       | True                                           |
| Está indexado             | False                                          |
| En el catálogo global      | False                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                   |
| Range-Lower            | \-                                             |
| Range-Upper            | \-                                             |
| Search-Flags           | 0x00000000                                     |
| System-Flags           | 0x00000010                                     |
| Clases usadas en        | [**Almacén de clases**](c-classstore.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Almacén de clases**](c-classstore.md)<br/> [**Punto de conexión de servicio**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Almacén de clases**](c-classstore.md)<br/> [**Punto de conexión de servicio**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Almacén de clases**](c-classstore.md)<br/> [**Punto de conexión de servicio**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Almacén de clases**](c-classstore.md)<br/> [**Punto de conexión de servicio**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                                            |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Almacén de clases**](c-classstore.md)<br/> [**Punto de conexión de servicio**](c-serviceconnectionpoint.md)<br/> |



 

 





