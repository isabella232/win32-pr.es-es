---
title: Atributo SAM-Account-Type
description: Este atributo contiene información sobre cada objeto de tipo de cuenta.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- SAM-Account-Type atributo AD Schema
- sAMAccountType esquema de AD de atributos
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997368"
---
# <a name="sam-account-type-attribute"></a>Atributo SAM-Account-Type

Este atributo contiene información sobre cada objeto de tipo de cuenta. Puede enumerar una lista de tipos de cuenta o puede usar la API Mostrar información para crear una lista. Dado que los equipos, las cuentas de usuario normales y las cuentas de confianza también se pueden enumerar como objetos de usuario, los valores de estas cuentas deben ser un intervalo contiguo.

Los valores posibles para este atributo son los siguientes:

-   \_Objeto de dominio Sam \_ 0X0
-   \_Objeto de Grupo SAM \_ 0x10000000
-   \_Objeto de \_ grupo de no seguridad Sam \_ \_ 0x10000001
-   \_Objeto de alias Sam \_ 0x20000000
-   \_Objeto de \_ alias de no seguridad Sam \_ \_ 0x20000001
-   \_Objeto de usuario Sam \_ 0x30000000
-   SAM \_ \_ 0x30000000 de cuenta de usuario normal \_
-   SAM \_ cuenta de equipo \_ 0x30000001
-   SAM de la \_ cuenta de confianza \_ 0x30000002
-   \_ \_ Grupo básico de la aplicación Sam \_
-   \_Grupo de consulta de aplicaciones Sam \_ \_ 0x40000001
-   \_Tipo de cuenta SAM \_ \_ máx.



| Entrada | Value |
|-------------------|-----------------------------------------------------------------|
| CN                | Tipo de cuenta SAM                                                |
| Nombre para mostrar de LDAP | sAMAccountType                                                  |
| Tamaño              | \-                                                              |
| Actualizar privilegio  | El sistema establece este valor.                                |
| Frecuencia de actualización  | Lo establece el sistema operativo cuando se crea el objeto. |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| System-ID-GUID    | 6e7b626c-64f2-11d0-afd2-00c04fd930c9                            |
| Sintaxis            | [**Enumeración**](s-enumeration.md)                            |



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
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Identificador de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Tiene un único valor       | True                                                         |
| Está indexado             | True                                                         |
| En el catálogo global      | True                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





