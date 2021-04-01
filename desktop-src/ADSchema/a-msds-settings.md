---
title: atributo MS-DS-Settings
description: Se utiliza para almacenar la configuración de un objeto. Su uso está determinado únicamente por el propietario del objeto. Se recomienda usarlo para almacenar pares de nombre/valor. Por ejemplo, color azul.
ms.assetid: 44e3a9e2-5528-4328-9cb7-1b6a4a77950a
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-DS-Settings
- atributo msDS-Settings esquema de AD
topic_type:
- apiref
api_name:
- ms-DS-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f466bd5aa5a904482ff9c84c1f818c12205f69c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906018"
---
# <a name="ms-ds-settings-attribute"></a>atributo MS-DS-Settings

Se utiliza para almacenar la configuración de un objeto. Su uso está determinado únicamente por el propietario del objeto. Se recomienda usarlo para almacenar pares de nombre/valor. Por ejemplo, color = Blue.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Configuración de MS-DS                              |
| Nombre para mostrar de LDAP | msDS-Settings                               |
| Tamaño              | \-                                          |
| Actualizar privilegio  | Administrador de dominio                        |
| Frecuencia de actualización  | Cada vez que cambian los valores de configuración.       |
| Attribute-Id      | 1.2.840.113556.1.4.1697                     |
| System-ID-GUID    | 0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | False                                                                                                                     |
| Tiene un único valor       | False                                                                                                                     |
| Está indexado             | False                                                                                                                     |
| En el catálogo global      | False                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Clases usadas en        | [**Configuración de la aplicación**](c-applicationsettings.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Tiene un único valor       | False                                                            |
| Está indexado             | False                                                            |
| En el catálogo global      | False                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000000                                                       |
| Clases usadas en        | [**Configuración de la aplicación**](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | False                                                                                                                     |
| Tiene un único valor       | False                                                                                                                     |
| Está indexado             | False                                                                                                                     |
| En el catálogo global      | False                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Clases usadas en        | [**Configuración de la aplicación**](c-applicationsettings.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | False                                                                                                                     |
| Tiene un único valor       | False                                                                                                                     |
| Está indexado             | False                                                                                                                     |
| En el catálogo global      | False                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Clases usadas en        | [**Configuración de la aplicación**](c-applicationsettings.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | False                                                                                                                     |
| Tiene un único valor       | False                                                                                                                     |
| Está indexado             | False                                                                                                                     |
| En el catálogo global      | False                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Clases usadas en        | [**Configuración de la aplicación**](c-applicationsettings.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                        |
| MAPI-Id                | \-                                                                                                                        |
| System-Only            | False                                                                                                                     |
| Tiene un único valor       | False                                                                                                                     |
| Está indexado             | False                                                                                                                     |
| En el catálogo global      | False                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                              |
| Range-Lower            | \-                                                                                                                        |
| Range-Upper            | \-                                                                                                                        |
| Search-Flags           | 0x00000000                                                                                                                |
| System-Flags           | 0x00000000                                                                                                                |
| Clases usadas en        | [**Configuración de la aplicación**](c-applicationsettings.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> |



 

 





