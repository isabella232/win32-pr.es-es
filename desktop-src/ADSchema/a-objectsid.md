---
title: Object-Sid atributo)
description: Valor binario que especifica el identificador de seguridad (SID) del usuario. El SID es un valor único que se usa para identificar al usuario como una entidad de seguridad.
ms.assetid: 78ef0158-f59e-43df-b3fc-fb0f709936f6
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Object-Sid
- atributo objectSid-esquema de AD
topic_type:
- apiref
api_name:
- Object-Sid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b536650177f873cbbc349096e84c3de274b8d376
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151605"
---
# <a name="object-sid-attribute"></a>Object-Sid atributo)

Valor binario que especifica el identificador de seguridad (SID) del usuario. El SID es un valor único que se usa para identificar al usuario como una entidad de seguridad.



| Entrada | Value |
|-------------------|--------------------------------------------------------------|
| CN                | Object-Sid                                                   |
| Nombre para mostrar de LDAP | objectSid                                                    |
| Tamaño              | \-                                                           |
| Actualizar privilegio  | El sistema establece este valor.                             |
| Frecuencia de actualización  | El sistema establece este valor cuando se crea la cuenta. |
| Attribute-Id      | 1.2.840.113556.1.4.146                                       |
| System-ID-GUID    | bf9679e8-0de6-11d0-a285-00aa003049e2                         |
| Sintaxis            | [**Cadena (SID)**](s-string-sid.md)                          |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                      |
| Tiene un único valor       | True                                                                                                                                                                                                                                                       |
| Está indexado             | True                                                                                                                                                                                                                                                       |
| En el catálogo global      | True                                                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| Tiene un único valor       | True                                                                                                                                                                                                                                                       |
| Está indexado             | True                                                                                                                                                                                                                                                       |
| En el catálogo global      | True                                                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                               |
| MAPI-Id                | 0x8027                                                                                                                                                                                           |
| System-Only            | True                                                                                                                                                                                             |
| Tiene un único valor       | True                                                                                                                                                                                             |
| Está indexado             | True                                                                                                                                                                                             |
| En el catálogo global      | True                                                                                                                                                                                             |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                |
| Range-Upper            | 28                                                                                                                                                                                               |
| Search-Flags           | 0x00000009                                                                                                                                                                                       |
| System-Flags           | 0x00000012                                                                                                                                                                                       |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MS-DS-BIND-proxy**](c-msds-bindproxy.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| Tiene un único valor       | True                                                                                                                                                                                                                                                       |
| Está indexado             | True                                                                                                                                                                                                                                                       |
| En el catálogo global      | True                                                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| Tiene un único valor       | True                                                                                                                                                                                                                                                       |
| Está indexado             | True                                                                                                                                                                                                                                                       |
| En el catálogo global      | True                                                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| Tiene un único valor       | True                                                                                                                                                                                                                                                       |
| Está indexado             | True                                                                                                                                                                                                                                                       |
| En el catálogo global      | True                                                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | True                                                                                                                                                                                                                                                       |
| Tiene un único valor       | True                                                                                                                                                                                                                                                       |
| Está indexado             | True                                                                                                                                                                                                                                                       |
| En el catálogo global      | True                                                                                                                                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Clases usadas en        | [**Entidad de seguridad externa**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





