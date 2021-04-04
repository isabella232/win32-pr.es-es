---
title: Pwd-Properties atributo)
description: Propiedades de contraseña. Parte de la Directiva de dominio. Un campo de bits para indicar la complejidad y las restricciones de almacenamiento.
ms.assetid: 9d73595f-508f-4562-a928-4833df977ab3
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Pwd-Properties
- pwdProperties esquema de AD de atributos
topic_type:
- apiref
api_name:
- Pwd-Properties
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d8338e1bb8279aa5b80e5edaa536c6a246e4912
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997370"
---
# <a name="pwd-properties-attribute"></a>Pwd-Properties atributo)

Propiedades de contraseña. Parte de la Directiva de dominio. Un campo de bits para indicar la complejidad y las restricciones de almacenamiento.



| Entrada | Value |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Pwd-Properties                                                                                                                                                                                                           |
| Nombre para mostrar de LDAP | pwdProperties                                                                                                                                                                                                            |
| Tamaño              | Entero. Contraseña de dominio \_ \_ complejo 1, \_ contraseña de dominio \_ sin \_ Anon \_ cambio 2, contraseña de dominio \_ sin borrar, cambio \_ \_ \_ 4, administradores de bloqueo de dominio \_ \_ 8, \_ almacén de contraseñas de dominio \_ \_ ClearText 16, \_ cambio de contraseña de denegación de dominio \_ \_ 32 |
| Actualizar privilegio  | Administrador de dominio                                                                                                                                                                                                     |
| Frecuencia de actualización  | Cuando cambia la Directiva de un usuario.                                                                                                                                                                                      |
| Attribute-Id      | 1.2.840.113556.1.4.93                                                                                                                                                                                                    |
| System-ID-GUID    | bf967a0b-0de6-11d0-a285-00aa003049e2                                                                                                                                                                                     |
| Sintaxis            | [**Enumeración**](s-enumeration.md)                                                                                                                                                                                     |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



 

 





