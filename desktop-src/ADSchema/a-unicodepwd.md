---
title: Unicode-Pwd atributo
description: Contraseña del usuario en formato un Windows NT un way (OWF). Windows 2000 usa el Windows NT OWF. Esta propiedad solo la usa el sistema operativo. Tenga en cuenta que no puede volver a derivar la contraseña sin borrar del formulario OWF de la contraseña.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Unicode-Pwd esquema de AD del atributo
- Esquema de AD del atributo unicodePwd
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e21929cf41b58688f768ada0b608ca3ef0892a4a54043c30f5cac2d5a72258b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681092"
---
# <a name="unicode-pwd-attribute"></a>Unicode-Pwd atributo

Contraseña del usuario en formato un Windows NT un way (OWF). Windows 2000 usa el Windows NT OWF. Esta propiedad solo la usa el sistema operativo. Tenga en cuenta que no puede volver a derivar la contraseña sin borrar del formulario OWF de la contraseña.



| Entrada | Value |
|-------------------|------------------------------------------------------------------------------|
| CN                | Unicode-Pwd                                                                  |
| Ldap-Display-Name | unicodePwd                                                                   |
| Size              | \-                                                                           |
| Privilegio actualizar  | Administrador de dominio o propietario de la cuenta.                                       |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que es necesario cambiar la contraseña. |
| Attribute-Id      | 1.2.840.113556.1.4.90                                                        |
| System-Id-Guid    | bf9679e1-0de6-11d0-a285-00aa003049e2                                         |
| Sintaxis            | [**Object(Replica-Link)**](s-object-replica-link.md)                        |



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
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
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
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Es de un solo valor       | True                                                              |
| Está indexado             | False                                                             |
| En el catálogo global      | False                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
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
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
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
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
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
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



 

 





