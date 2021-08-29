---
title: Atributo Locale-ID
description: Este atributo contiene una lista de los id. de configuración regional admitidos por esta aplicación. Un identificador de configuración regional representa una ubicación geográfica, como un país o región, una ciudad, un condado, y así sucesivamente.
ms.assetid: 60629155-2bdf-4080-bb88-c8db749ef954
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Locale-ID
- Esquema de AD del atributo localeID
topic_type:
- apiref
api_name:
- Locale-ID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee343011d8e8c2dda9e4aa20f0a64eceb43071c9b58e03678bc418c9b11a400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705875"
---
# <a name="locale-id-attribute"></a>Atributo Locale-ID

Este atributo contiene una lista de los id. de configuración regional admitidos por esta aplicación. Un identificador de configuración regional representa una ubicación geográfica, como un país o región, una ciudad, un condado, y así sucesivamente.



| Entrada | Valor |
|-------------------|----------------------------------------------------------------------------|
| CN                | Locale-ID                                                                  |
| Ldap-Display-Name | localeID                                                                   |
| Size              | 4 bytes                                                                    |
| Privilegio actualizar  | Administrador de dominio o propietario de la cuenta.                                     |
| Frecuencia de actualización  | Cuando se crea el registro de usuario y cada vez que es necesario cambiar la localidad. |
| Attribute-Id      | 1.2.840.113556.1.4.58                                                      |
| System-Id-Guid    | bf9679a1-0de6-11d0-a285-00aa003049e2                                       |
| Syntax            | [**Enumeración**](s-enumeration.md)                                       |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Clases usadas en        | [**Registro de categoría**](c-categoryregistration.md)<br/> [**Registro de paquetes**](c-packageregistration.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Clases usadas en        | [**Registro de categoría**](c-categoryregistration.md)<br/> [**Registro de paquetes**](c-packageregistration.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Clases usadas en        | [**Registro de categoría**](c-categoryregistration.md)<br/> [**Registro de paquetes**](c-packageregistration.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Clases usadas en        | [**Registro de categoría**](c-categoryregistration.md)<br/> [**Registro de paquetes**](c-packageregistration.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Clases usadas en        | [**Registro de categoría**](c-categoryregistration.md)<br/> [**Registro de paquetes**](c-packageregistration.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                                 |
| Es de un solo valor       | Falso                                                                                                                                                                 |
| Está indexado             | Falso                                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                                            |
| Clases usadas en        | [**Registro de categoría**](c-categoryregistration.md)<br/> [**Registro de paquetes**](c-packageregistration.md)<br/> [**Usuario**](c-user.md)<br/> |



 

 





