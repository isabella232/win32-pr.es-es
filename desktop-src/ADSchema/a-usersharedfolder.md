---
title: Atributo User-Shared-Folder
description: Especifica una ruta de acceso UNC a la carpeta de documentos compartidos del usuario. La ruta de acceso debe ser una ruta de acceso UNC de red con el formato \\ \\ Server Share \\ \\ Directory. Este valor puede ser una cadena null.
ms.assetid: 23b4177a-0a05-4111-affe-d81bc115580d
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo User-Shared-Folder
- Esquema de AD del atributo userSharedFolder
topic_type:
- apiref
api_name:
- User-Shared-Folder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3bcb2732fbaec9ac06db1bae3f07b03cac2018a4f88209b5391bd4a84b7836
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021993"
---
# <a name="user-shared-folder-attribute"></a>Atributo User-Shared-Folder

Especifica una ruta de acceso UNC a la carpeta de documentos compartidos del usuario. La ruta de acceso debe ser una ruta de acceso UNC de red con el formato **\\\\** _Server_ *_\\_* _Share_ *_\\_* _Directory_. Este valor puede ser una cadena null.



| Entrada | Value |
|-------------------|-----------------------------------------------------------------------------------|
| CN                | User-Shared-Folder                                                                |
| Ldap-Display-Name | userSharedFolder                                                                  |
| Size              | \-                                                                                |
| Privilegio actualizar  | Administrador de dominio o propietario de la cuenta.                                            |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que es necesario cambiar la carpeta compartida. |
| Attribute-Id      | 1.2.840.113556.1.4.751                                                            |
| System-Id-Guid    | 9a9a021f-4a5b-11d1-a9c3-0000f80367c1                                              |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                       |



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
| Search-Flags           | 0x00000000                        |
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



 

 





