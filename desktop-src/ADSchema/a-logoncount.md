---
title: Logon-Count atributo)
description: El número de veces que la cuenta ha iniciado sesión correctamente. Un valor de 0 indica que el valor es desconocido.
ms.assetid: 8b12bea7-dfc3-46e3-a4a2-92b5f1239b98
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Logon-Count
- logonCount esquema de AD de atributos
topic_type:
- apiref
api_name:
- Logon-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6ba7865cb3b90f42ede71b169f98f8ce45e722d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906071"
---
# <a name="logon-count-attribute"></a>Logon-Count atributo)

El número de veces que la cuenta ha iniciado sesión correctamente. Un valor de 0 indica que el valor es desconocido.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Logon-Count                          |
| Nombre para mostrar de LDAP | logonCount                           |
| Tamaño              | 4 bytes                              |
| Actualizar privilegio  | Administrador de dominio                 |
| Frecuencia de actualización  | Cada vez que el usuario inicia sesión.          |
| Attribute-Id      | 1.2.840.113556.1.4.169               |
| System-ID-GUID    | bf9679aa-0de6-11d0-a285-00aa003049e2 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**User**](c-user.md)<br/> |



## <a name="remarks"></a>Observaciones

Este atributo no se replica y se mantiene en cada controlador de dominio del dominio. Para obtener un valor preciso para el número total de intentos de inicio de sesión correctos del usuario en el dominio, se deben consultar todos los controladores de dominio del dominio y se debe usar la suma de los valores. Tenga en cuenta que el atributo no se replica, por lo tanto, los controladores de dominio que se retiran también pueden haber contado los inicios de sesión del usuario y estos no aparecerán en el recuento.

> [!IMPORTANT]
> Debido a la compatibilidad con las versiones de 16 bits de LAN Manager, el atributo tiene un límite superior de 65535. Una vez alcanzado este límite, no se puede usar como un indicador de la actividad del usuario en este controlador de dominio.

 

 

 





