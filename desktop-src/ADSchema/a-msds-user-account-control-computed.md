---
title: atributo de calculado de la cuenta de usuario de MS-DS-control
description: msDS-User-Account-Control-Compute es muy similar a userAccountControl, pero el valor del atributo puede contener bits adicionales que no se conservan.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos calculados de Microsoft-DS-User-Account-control
- msDS-User-Account-Control-esquema de AD de atributos calculados
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658848"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a>atributo de calculado de la cuenta de usuario de MS-DS-control

**MSDS-User-Account-Control-Compute** es muy similar a [**UserAccountControl**](a-useraccountcontrol.md), pero el valor del atributo puede contener bits adicionales que no se conservan. Entre los bits calculados se incluyen los siguientes.



| Value                | Nombre (definido en iAds. h)                     |
|----------------------|----------------------------------------------|
| 0x0010<br/>    | **bloqueo de fi \_**<br/>                   |
| 0x800000<br/>  | **la contraseña de la up ha \_ \_ expirado**<br/>         |
| 0x4000000<br/> | **\_cuenta de \_ secretos \_ parciales de la up**<br/> |
| 0x8000000<br/> | **FI \_ usar \_ \_ claves AES**<br/>            |



 

La lista completa de bits que [**User-Account-Control**](a-useraccountcontrol.md) y, por lo tanto, **MSDS-User-Account-Control-Compute** también puede contener en la página de referencia de **User-Account-Control** (asignada a través de [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset) o en las páginas de referencia de administración de redes de la estructura [**User \_ info \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) .



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-DS-User-Account-control-calculado  |
| Nombre para mostrar de LDAP | msDS-User-Account-control-calculado   |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1460              |
| System-ID-GUID    | 2cc4b836-b63f-4940-8d23-ea7acf06af56 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Tiene un único valor       | True                                                              |
| Está indexado             | False                                                             |
| En el catálogo global      | False                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000014                                                        |
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
| System-Flags           | 0x00000014                        |
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
| System-Flags           | 0x00000014                        |
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
| System-Flags           | 0x00000014                        |
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
| System-Flags           | 0x00000014                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



 

