---
title: Object-Sid atributo
description: Valor binario que especifica el identificador de seguridad (SID) del usuario. El SID es un valor único que se usa para identificar al usuario como entidad de seguridad.
ms.assetid: 78ef0158-f59e-43df-b3fc-fb0f709936f6
ms.tgt_platform: multiple
keywords:
- Object-Sid esquema de AD del atributo
- ObjectSid attribute AD Schema
topic_type:
- apiref
api_name:
- Object-Sid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65bf21d8806d904185c01e8831b8597c6cd69424f82789c1e419ec38e3be4dd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442365"
---
# <a name="object-sid-attribute"></a>Object-Sid atributo

Valor binario que especifica el identificador de seguridad (SID) del usuario. El SID es un valor único que se usa para identificar al usuario como entidad de seguridad.



| Entrada | Value |
|-------------------|--------------------------------------------------------------|
| CN                | Object-Sid                                                   |
| Ldap-Display-Name | objectSid                                                    |
| Size              | \-                                                           |
| Privilegio actualizar  | El sistema establece este valor.                             |
| Frecuencia de actualización  | El sistema establece este valor cuando se crea la cuenta. |
| Attribute-Id      | 1.2.840.113556.1.4.146                                       |
| System-Id-Guid    | bf9679e8-0de6-11d0-a285-00aa003049e2                         |
| Syntax            | [**String(Sid)**](s-string-sid.md)                          |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                      |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                       |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                       |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Verdadero                                                                                                                                                                                                                                                       |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                       |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                       |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                               |
| MAPI-Id                | 0x8027                                                                                                                                                                                           |
| System-Only            | Verdadero                                                                                                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                                                                                                             |
| Está indexado             | Verdadero                                                                                                                                                                                             |
| En el catálogo global      | Verdadero                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                |
| Range-Upper            | 28                                                                                                                                                                                               |
| Search-Flags           | 0x00000009                                                                                                                                                                                       |
| System-Flags           | 0x00000012                                                                                                                                                                                       |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**ms-DS-Bind-Proxy**](c-msds-bindproxy.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Verdadero                                                                                                                                                                                                                                                       |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                       |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                       |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Verdadero                                                                                                                                                                                                                                                       |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                       |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                       |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Verdadero                                                                                                                                                                                                                                                       |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                       |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                       |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Verdadero                                                                                                                                                                                                                                                       |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                       |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                       |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated-User**](c-msmqmigrateduser.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





