---
title: Security-Identifier atributo
description: Valor único de longitud variable que se usa para identificar una cuenta de usuario, una cuenta de grupo o una sesión de inicio de sesión a la que se aplica una ACE.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Security-Identifier esquema de AD del atributo
- Esquema de AD del atributo securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f15449127dd11e7e0ebfef9f63d8e79470ed662377cbdd1929ed072b2502dae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836875"
---
# <a name="security-identifier-attribute"></a>Security-Identifier atributo

Valor único de longitud variable que se usa para identificar una cuenta de usuario, una cuenta de grupo o una sesión de inicio de sesión a la que se aplica una ACE.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Security-Identifier                  |
| Ldap-Display-Name | securityIdentifier                   |
| Size              | \-                                   |
| Privilegio actualizar  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.121               |
| System-Id-Guid    | bf967a2f-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**String(Sid)**](s-string-sid.md)  |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                              |
| Está indexado             | Falso                                                                                                             |
| En el catálogo global      | Falso                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                              |
| Está indexado             | Falso                                                                                                             |
| En el catálogo global      | Verdadero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                              |
| Está indexado             | Falso                                                                                                             |
| En el catálogo global      | Verdadero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                              |
| Está indexado             | Falso                                                                                                             |
| En el catálogo global      | Verdadero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                              |
| Está indexado             | Falso                                                                                                             |
| En el catálogo global      | Verdadero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Es de un solo valor       | Verdadero                                                                                                              |
| Está indexado             | Falso                                                                                                             |
| En el catálogo global      | Verdadero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> [**Dominio de confianza**](c-trusteddomain.md)<br/> |



 

 





