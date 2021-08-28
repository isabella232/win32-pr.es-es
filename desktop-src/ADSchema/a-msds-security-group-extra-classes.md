---
title: Atributo ms-DS-Security-Group-Extra-Classes
description: Nombres comunes de las clases no estándar que se pueden agregar a un grupo de seguridad a través del Usuarios y equipos de Active Directory complemento.
ms.assetid: 3808cb03-3d54-46ca-bad8-23120ed2ca07
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DS-Security-Group-Extra-Classes
- Esquema de AD del atributo msDS-Security-Group-Extra-Classes
topic_type:
- apiref
api_name:
- ms-DS-Security-Group-Extra-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c64746abd1114ebb3e4a97cf912a35ac730d6062721e8a11d67103d1fe82b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544735"
---
# <a name="ms-ds-security-group-extra-classes-attribute"></a>Atributo ms-DS-Security-Group-Extra-Classes

Nombres comunes de las clases no estándar que se pueden agregar a un grupo de seguridad a través del Usuarios y equipos de Active Directory complemento.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | ms-DS-Security-Group-Extra-Classes          |
| Ldap-Display-Name | msDS-Security-Group-Extra-Classes           |
| Size              | \-                                          |
| Actualizar privilegios  | Administrador de dominio                        |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.1688                     |
| System-Id-Guid    | 4f146ae8-a4fe-4801-a731-f51848a4f4e4        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Id. de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| Es de un solo valor       | Falso                                               |
| Está indexado             | Falso                                               |
| En el catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-Configuración**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Id. de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| Es de un solo valor       | Falso                                               |
| Está indexado             | Falso                                               |
| En el catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-Configuración**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Id. de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| Es de un solo valor       | Falso                                               |
| Está indexado             | Falso                                               |
| En el catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-Configuración**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Id. de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| Es de un solo valor       | Falso                                               |
| Está indexado             | Falso                                               |
| En el catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-Configuración**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Id. de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| Es de un solo valor       | Falso                                               |
| Está indexado             | Falso                                               |
| En el catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-Configuración**](c-dsuisettings.md)<br/> |



## <a name="remarks"></a>Comentarios

En la lista siguiente se identifican las clases estándar que se pueden agregar a un grupo a través del Usuarios y equipos de Active Directory complemento.

-   [**Group (Grupo)**](c-group.md)
-   [**Usuario**](c-user.md)
-   [**inetOrgPerson**](c-inetorgperson.md)
-   [**Contacto**](c-contact.md)
-   [**Computer**](c-computer.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ms-DS-non-Security-Group-Extra-Classes**](a-msds-non-security-group-extra-classes.md)
</dt> </dl>

 

 





