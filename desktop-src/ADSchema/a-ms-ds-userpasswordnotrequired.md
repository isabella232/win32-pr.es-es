---
title: atributo MS-DS-User-Password-Not-Required
description: Indica si se requiere una contraseña para la cuenta a la que hace referencia este atributo.
ms.assetid: 86779c6f-d05c-409a-afe4-99ebf7c0593e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributos MS-DS-User-Password-Not-Required
- Esquema de AD del atributo MS-DS-UserPasswordNotRequired
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Not-Required
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8ebb439af9a960d2dc0721940d9f4d2ab852b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151851"
---
# <a name="ms-ds-user-password-not-required-attribute"></a>atributo MS-DS-User-Password-Not-Required

Indica si se requiere una contraseña para la cuenta a la que hace referencia este atributo. True si no se requiere una contraseña; en caso contrario, false.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-DS-User-Password-Not-Required     |
| Nombre para mostrar de LDAP | MS-DS-UserPasswordNotRequired        |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1854              |
| System-ID-GUID    | 8f066172-a25e-4f53-8dcd-0a67d5fb883d |
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
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**Objeto MS-DS-Bindable**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Observaciones

En ADAM, este atributo reemplaza la marca de [**ADS \_ \_ \_ NOTREQD passwd passwd**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) del atributo [**UserAccountControl**](a-useraccountcontrol.md) .

 

