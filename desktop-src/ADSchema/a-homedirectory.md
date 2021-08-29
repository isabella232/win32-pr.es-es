---
title: Home-Directory atributo
description: Directorio principal de la cuenta.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Home-Directory esquema de AD del atributo
- Esquema de AD del atributo homeDirectory
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ef4ef612bfb2e91184d0e442115f712496f8bd788bb441bba7e7caa388031b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119305235"
---
# <a name="home-directory-attribute"></a>Home-Directory atributo

Directorio principal de la cuenta. Si [**homeDrive**](a-homedrive.md) está establecido y especifica una letra de unidad, **homeDirectory** debe ser una ruta de acceso UNC. De lo contrario, **homeDirectory** es una ruta de acceso local completa que incluye la letra de unidad (por ejemplo, *DriveLetter*:**\\ carpeta**_de_* _\\_ * _directorios)._ Este valor puede ser una cadena null.



| Entrada | Value |
|-------------------|------------------------------------------------------------------------------------|
| CN                | Home-Directory                                                                     |
| Ldap-Display-Name | homeDirectory                                                                      |
| Size              | \-                                                                                 |
| Privilegio actualizar  | Administrador de dominio                                                               |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que es necesario cambiar el directorio principal. |
| Attribute-Id      | 1.2.840.113556.1.4.44                                                              |
| System-Id-Guid    | bf967985-0de6-11d0-a285-00aa003049e2                                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                        |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Falso                             |
| En el catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Falso                             |
| En el catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| Es de un solo valor       | Verdadero                                                                                |
| Está indexado             | Falso                                                                               |
| En el catálogo global      | Falso                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| Es de un solo valor       | Verdadero                                                                                |
| Está indexado             | Falso                                                                               |
| En el catálogo global      | Falso                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| Es de un solo valor       | Verdadero                                                                                |
| Está indexado             | Falso                                                                               |
| En el catálogo global      | Falso                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| Es de un solo valor       | Verdadero                                                                                |
| Está indexado             | Falso                                                                               |
| En el catálogo global      | Falso                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**homeDrive**](a-homedrive.md)
</dt> </dl>

 

 





