---
title: Atributo Physical-Delivery-Office-Name
description: Contiene la ubicación de la oficina en el lugar de negocio del usuario.
ms.assetid: a6be61bf-9a9a-4b97-bdf8-894c173efadd
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Physical-Delivery-Office-Name
- Esquema de AD del atributo physicalDeliveryOfficeName
topic_type:
- apiref
api_name:
- Physical-Delivery-Office-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a574c7214f18d9cef46a64885ca2855fdaf3227a9dece159458d5f1cb07d8b7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647775"
---
# <a name="physical-delivery-office-name-attribute"></a>Atributo Physical-Delivery-Office-Name

Contiene la ubicación de la oficina en el lugar de negocio del usuario.



| Entrada | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| CN                | Physical-Delivery-Office-Name                                                       |
| Ldap-Display-Name | physicalDeliveryOfficeName                                                          |
| Size              | \-                                                                                  |
| Privilegio actualizar  | Administrador de dominio o propietario de la cuenta.                                              |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cada vez que es necesario cambiar la ubicación de la oficina. |
| Attribute-Id      | 2.5.4.19                                                                            |
| System-Id-Guid    | bf9679f7-0de6-11d0-a285-00aa003049e2                                                |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                         |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                           |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                            |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                            |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                             |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                               |
| MAPI-Id                | 0x3A19                                                                                                           |
| System-Only            | Falso                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                             |
| Está indexado             | Verdadero                                                                                                             |
| En el catálogo global      | Falso                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona residencial**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Falso                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Organización**](c-organization.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Rol organizativo**](c-organizationalrole.md)<br/> [**Unidad organizativa**](c-organizationalunit.md)<br/> [**Persona con residencia**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





