---
title: atributo MS-IIS-FTP-dir
description: Este atributo determina el directorio principal del usuario en relación con el recurso compartido del servidor de archivos. Se usa junto con MS-IIS-FTP-root para determinar el directorio particular del usuario FTP.
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-IIS-FTP-dir
- msIIS-FTPDir atributo AD Schema
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3067476e7dc275dbe14471d6c3c98fa5445a9dfe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535986"
---
# <a name="ms-iis-ftp-dir-attribute"></a>atributo MS-IIS-FTP-dir

Este atributo determina el directorio principal del usuario en relación con el recurso compartido del servidor de archivos. Se usa junto con MS-IIS-FTP-root para determinar el directorio particular del usuario FTP.



| Entrada | Value |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| CN                | MS-IIS-FTP-dir                                                                                                                  |
| Nombre para mostrar de LDAP | msIIS-FTPDir                                                                                                                    |
| Tamaño              | 30-50 caracteres (15-25 caracteres Unicode para cada propiedad)                                                                   |
| Actualizar privilegio  | Administrador de dominio & sistema local                                                                                             |
| Frecuencia de actualización  | Esta propiedad se establece cuando el administrador crea el sitio web y establece el aislamiento FTP. Rara vez va a cambiar después de eso. |
| Attribute-Id      | 1.2.840.113556.1.4.1786                                                                                                         |
| System-ID-GUID    | 8a5c99e9-2230-46eb-b8e8-e59d712eb9ee                                                                                            |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

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
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------|
| Identificador de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Tiene un único valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                      |
| Range-Lower            | 1                                 |
| Range-Upper            | 256                               |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



 

 





