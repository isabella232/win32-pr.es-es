---
title: atributo MS-DS-Security-Group-de clases adicionales
description: Los nombres comunes de las clases no estándar que se pueden agregar a un grupo de seguridad a través del complemento usuarios y equipos de Active Directory.
ms.assetid: 3808cb03-3d54-46ca-bad8-23120ed2ca07
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos de clases de MS-DS-Security-Group-extra
- msDS-Security-Group-clases esquema de AD de atributo
topic_type:
- apiref
api_name:
- ms-DS-Security-Group-Extra-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3860cc80c669eaad30262cce63aff6dca3a2a8f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151806"
---
# <a name="ms-ds-security-group-extra-classes-attribute"></a>atributo MS-DS-Security-Group-de clases adicionales

Los nombres comunes de las clases no estándar que se pueden agregar a un grupo de seguridad a través del complemento usuarios y equipos de Active Directory.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | MS-DS-Security-Group-clases adicionales          |
| Nombre para mostrar de LDAP | msDS-Security-Group-extra-classes           |
| Tamaño              | \-                                          |
| Actualizar privilegio  | Administrador de dominio                        |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.1688                     |
| System-ID-GUID    | 4f146ae8-a4fe-4801-a731-f51848a4f4e4        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Identificador de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | False                                               |
| Tiene un único valor       | False                                               |
| Está indexado             | False                                               |
| En el catálogo global      | False                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-configuración**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Identificador de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | False                                               |
| Tiene un único valor       | False                                               |
| Está indexado             | False                                               |
| En el catálogo global      | False                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-configuración**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Identificador de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | False                                               |
| Tiene un único valor       | False                                               |
| Está indexado             | False                                               |
| En el catálogo global      | False                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-configuración**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Identificador de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | False                                               |
| Tiene un único valor       | False                                               |
| Está indexado             | False                                               |
| En el catálogo global      | False                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-configuración**](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------|
| Identificador de vínculo                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | False                                               |
| Tiene un único valor       | False                                               |
| Está indexado             | False                                               |
| En el catálogo global      | False                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Clases usadas en        | [**DS-UI-configuración**](c-dsuisettings.md)<br/> |



## <a name="remarks"></a>Observaciones

En la lista siguiente se identifican las clases estándar que se pueden agregar a un grupo a través del complemento usuarios y equipos de Active Directory.

-   [**Group (Grupo)**](c-group.md)
-   [**User**](c-user.md)
-   [**inetOrgPerson**](c-inetorgperson.md)
-   [**Contacto**](c-contact.md)
-   [**Computer**](c-computer.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**MS-DS-non-Security-Group-extra-classes**](a-msds-non-security-group-extra-classes.md)
</dt> </dl>

 

 





