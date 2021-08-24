---
title: Atributo Bad-Pwd-Count
description: Número de veces que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta.
ms.assetid: 1161b0c1-1b28-4349-ad43-82ce68428c44
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Bad-Pwd-Count
- Esquema de AD del atributo badPwdCount
topic_type:
- apiref
api_name:
- Bad-Pwd-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 608e587627bd8b470582e247bc8586e7e1576a2ff865a64bd9bd6fb60bd07c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081929"
---
# <a name="bad-pwd-count-attribute"></a>Atributo Bad-Pwd-Count

Número de veces que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta. Un valor de 0 indica que el valor es desconocido.



| Entrada | Value |
|-------------------|-------------------------------------------|
| CN                | Bad-Pwd-Count                             |
| Ldap-Display-Name | badPwdCount                               |
| Size              | 4 bytes                                   |
| Privilegio actualizar  | El sistema establece este valor.          |
| Frecuencia de actualización  | Cada vez que el usuario escribe una contraseña incorrecta. |
| Attribute-Id      | 1.2.840.113556.1.4.12                     |
| System-Id-Guid    | bf96792e-0de6-11d0-a285-00aa003049e2      |
| Syntax            | [**Enumeración**](s-enumeration.md)      |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Verdadero                                                              |
| Es de un solo valor       | Verdadero                                                              |
| Está indexado             | Falso                                                             |
| En el catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000011                                                        |
| Clases usadas en        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="remarks"></a>Comentarios

Este atributo no se replica y se mantiene por separado en cada controlador de dominio del dominio.

Este atributo se restablece en un controlador de dominio específico cuando el usuario inicia sesión correctamente en ese controlador de dominio.

 

 





