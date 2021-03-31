---
title: Home-Directory atributo)
description: Directorio particular de la cuenta.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Home-Directory
- homeDirectory esquema de AD de atributos
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804789"
---
# <a name="home-directory-attribute"></a>Home-Directory atributo)

Directorio particular de la cuenta. Si [**HOMEDRIVE**](a-homedrive.md) se establece y especifica una letra de unidad, **HomeDirectory** debe ser una ruta de acceso UNC. De lo contrario, **HomeDirectory** es una ruta de acceso local completa que incluye la letra de unidad (por ejemplo, *letraDeUnidad ***: \\** carpeta del _directorio_* _\\_ * ). Este valor puede ser una cadena nula.



| Entrada | Value |
|-------------------|------------------------------------------------------------------------------------|
| CN                | Home-Directory                                                                     |
| Nombre para mostrar de LDAP | homeDirectory                                                                      |
| Tamaño              | \-                                                                                 |
| Actualizar privilegio  | Administrador de dominio                                                               |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que es necesario cambiar el directorio particular. |
| Attribute-Id      | 1.2.840.113556.1.4.44                                                              |
| System-ID-GUID    | bf967985-0de6-11d0-a285-00aa003049e2                                               |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                        |



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
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | False                                                                               |
| Tiene un único valor       | True                                                                                |
| Está indexado             | False                                                                               |
| En el catálogo global      | False                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Clases usadas en        | [**User**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | False                                                                               |
| Tiene un único valor       | True                                                                                |
| Está indexado             | False                                                                               |
| En el catálogo global      | False                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Clases usadas en        | [**User**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | False                                                                               |
| Tiene un único valor       | True                                                                                |
| Está indexado             | False                                                                               |
| En el catálogo global      | False                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Clases usadas en        | [**User**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | False                                                                               |
| Tiene un único valor       | True                                                                                |
| Está indexado             | False                                                                               |
| En el catálogo global      | False                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Clases usadas en        | [**User**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**homeDrive**](a-homedrive.md)
</dt> </dl>

 

 





