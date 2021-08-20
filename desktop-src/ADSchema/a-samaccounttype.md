---
title: Atributo SAM-Account-Type
description: Este atributo contiene información sobre cada objeto de tipo de cuenta.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo SAM-Account-Type
- Esquema de AD del atributo sAMAccountType
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132532af58eafa4950f049fb08ff7a4235cb49ac2b1f62fc832e308e7ab6d31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118423392"
---
# <a name="sam-account-type-attribute"></a>Atributo SAM-Account-Type

Este atributo contiene información sobre cada objeto de tipo de cuenta. Puede enumerar una lista de tipos de cuenta o puede usar Display Information API para crear una lista. Dado que los equipos, las cuentas de usuario normales y las cuentas de confianza también se pueden enumerar como objetos de usuario, los valores de estas cuentas deben ser un intervalo contiguo.

Los valores posibles para este atributo son los siguientes:

-   Sam \_ DOMAIN \_ OBJECT 0x0
-   Sam \_ GROUP \_ OBJECT 0x10000000
-   SAM \_ NON SECURITY GROUP OBJECT \_ \_ \_ 0x10000001
-   OBJETO \_ DE ALIAS SAM \_ 0x20000000
-   SAM \_ NON SECURITY ALIAS OBJECT \_ \_ \_ 0x20000001
-   Sam \_ USER \_ OBJECT 0x30000000
-   CUENTA DE USUARIO NORMAL DE SAM \_ \_ \_ 0x30000000
-   CUENTA \_ DE MÁQUINA SAM \_ 0x30000001
-   CUENTA \_ DE CONFIANZA DE SAM \_ 0x30000002
-   APLICACIÓN \_ SAM BASIC GROUP \_ \_ 0x40000000
-   GRUPO \_ DE CONSULTAS DE APLICACIONES SAM \_ \_ 0x40000001
-   TIPO \_ DE CUENTA SAM MAX \_ \_ 0x7fffffff



| Entrada | Valor |
|-------------------|-----------------------------------------------------------------|
| CN                | SAM-Account-Type                                                |
| Ldap-Display-Name | sAMAccountType                                                  |
| Size              | \-                                                              |
| Actualizar privilegios  | El sistema establece este valor.                                |
| Frecuencia de actualización  | Lo establece el sistema operativo cuando se crea el objeto . |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| System-Id-Guid    | 6e7b626c-64f2-11d0-afd2-00c04fd930c9                            |
| Syntax            | [**Enumeración**](s-enumeration.md)                            |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Verdadero                                                         |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





