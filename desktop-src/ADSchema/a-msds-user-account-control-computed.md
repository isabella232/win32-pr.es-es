---
title: Atributo ms-DS-User-Account-Control-Computed
description: msDS-User-Account-Control-Computed es muy parecido a userAccountControl, pero el valor del atributo puede contener bits adicionales que no se conservan.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DS-User-Account-Control-Computed
- Esquema de AD del atributo msDS-User-Account-Control-Computed
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8747bddccdfa65222072592b7f418fd35529d987f9903d71cddf5e01556fec53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763265"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a>Atributo ms-DS-User-Account-Control-Computed

**msDS-User-Account-Control-Computed** es muy parecido a [**userAccountControl,**](a-useraccountcontrol.md)pero el valor del atributo puede contener bits adicionales que no se conservan. Los bits calculados incluyen lo siguiente.



| Value                | Nombre (definido en Iads.h)                     |
|----------------------|----------------------------------------------|
| 0x0010<br/>    | **UF \_ LOCKOUT**<br/>                   |
| 0x800000<br/>  | **CONTRASEÑA DE UF \_ \_ EXPIRADA**<br/>         |
| 0x4000000<br/> | **CUENTA DE \_ SECRETOS \_ PARCIALES \_ DE UF**<br/> |
| 0x8000000<br/> | **UF \_ USE \_ CLAVES AES \_**<br/>            |



 

La lista completa de bits que [**User-Account-Control**](a-useraccountcontrol.md) y, por **tanto, msDS-User-Account-Control-Computed** también puede contener, puede encontrarse en la página de referencia **User-Account-Control** (asignada a través del conjunto de marcas [ADSI)](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) o en las páginas de referencia de administración de red para la estructura [**\_ \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) de información de usuario.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Control-Computed  |
| Ldap-Display-Name | msDS-User-Account-Control-Computed   |
| Size              | \-                                   |
| Privilegio actualizar  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1460              |
| System-Id-Guid    | 2cc4b836-b63f-4940-8d23-ea7acf06af56 |
| Syntax            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

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
| System-Flags           | 0x00000014                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Es de un solo valor       | Verdadero                                                              |
| Está indexado             | Falso                                                             |
| En el catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000014                                                        |
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
| System-Flags           | 0x00000014                        |
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
| System-Flags           | 0x00000014                        |
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
| System-Flags           | 0x00000014                        |
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
| System-Flags           | 0x00000014                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



 

