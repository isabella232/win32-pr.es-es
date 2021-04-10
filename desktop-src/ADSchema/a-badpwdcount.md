---
title: Atributo Bad-pwd-Count
description: El número de veces que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta.
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo incorrecto-pwd-Count
- badPwdCount esquema de AD de atributos
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3a406058737773781874a81e9968786e1523d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151487"
---
# <a name="bad-pwd-count-attribute"></a>Atributo Bad-pwd-Count

El número de veces que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta. Un valor de 0 indica que el valor es desconocido.



| Entrada | Value |
|-------------------|-------------------------------------------|
| CN                | Incorrecto: PWD-Count                             |
| Nombre para mostrar de LDAP | badPwdCount                               |
| Tamaño              | 4 bytes                                   |
| Actualizar privilegio  | El sistema establece este valor.          |
| Frecuencia de actualización  | Cada vez que el usuario escribe una contraseña incorrecta. |
| Attribute-Id      | 1.2.840.113556.1.4.12                     |
| System-ID-GUID    | bf96792e-0de6-11d0-a285-00aa003049e2      |
| Sintaxis            | [**Enumeración**](s-enumeration.md)      |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | True                                                              |
| Tiene un único valor       | True                                                              |
| Está indexado             | False                                                             |
| En el catálogo global      | False                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000011                                                        |
| Clases usadas en        | [**Objeto MS-DS-Bindable**](c-msds-bindableobject.md)<br/> |



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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="remarks"></a>Observaciones

Este atributo no se replica y se mantiene por separado en cada controlador de dominio del dominio.

Este atributo se restablece en un controlador de dominio específico cuando el usuario inicia sesión correctamente en ese controlador de dominio.

 

 





