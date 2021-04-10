---
title: atributo MS-DS-User-Password-Expired
description: Indica si ha expirado la contraseña de la cuenta a la que hace referencia este atributo.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos MS-DS-User-Password-Expired
- Esquema de AD de atributo msDS-UserPasswordExpired
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d99143c470e58d1b1cb5e0cbd7e5302618ff0a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104274593"
---
# <a name="ms-ds-user-password-expired-attribute"></a>atributo MS-DS-User-Password-Expired

Indica si ha expirado la contraseña de la cuenta a la que hace referencia este atributo. True si la contraseña ha expirado; en caso contrario, false.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-DS-User-Password-Expired          |
| Nombre para mostrar de LDAP | msDS-UserPasswordExpired             |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| System-ID-GUID    | 565c7ab5-e13e-47f6-abb5-de741806f125 |
| Sintaxis            | [**Booleano**](s-boolean.md)         |



## <a name="implementations"></a>Implementaciones

-   [**ADAM**](#adam)

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



## <a name="remarks"></a>Observaciones

En ADAM, este atributo reemplaza la marca [**ADS \_ up \_ password \_ Expired**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) en el atributo [**UserAccountControl**](a-useraccountcontrol.md) .

 

