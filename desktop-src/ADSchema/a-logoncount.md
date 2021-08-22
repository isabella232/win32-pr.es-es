---
title: Logon-Count atributo
description: Número de veces que la cuenta ha iniciado sesión correctamente. Un valor de 0 indica que el valor es desconocido.
ms.assetid: 8b12bea7-dfc3-46e3-a4a2-92b5f1239b98
ms.tgt_platform: multiple
keywords:
- Logon-Count esquema de AD de atributo
- Esquema de AD del atributo logonCount
topic_type:
- apiref
api_name:
- Logon-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac737353c08bc937f62212e98358909c8619873c51775b1ad15f802bdcc46a52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301585"
---
# <a name="logon-count-attribute"></a>Logon-Count atributo

Número de veces que la cuenta ha iniciado sesión correctamente. Un valor de 0 indica que el valor es desconocido.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Logon-Count                          |
| Ldap-Display-Name | logonCount                           |
| Size              | 4 bytes                              |
| Actualizar privilegios  | Administrador de dominio                 |
| Frecuencia de actualización  | Cada vez que el usuario inicia sesión.          |
| Attribute-Id      | 1.2.840.113556.1.4.169               |
| System-Id-Guid    | bf9679aa-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeración**](s-enumeration.md) |



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
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Es de un solo valor       | True                              |
| Está indexado             | False                             |
| En el catálogo global      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="remarks"></a>Comentarios

Este atributo no se replica y se mantiene en cada controlador de dominio del dominio. Para obtener un valor preciso para el número total de intentos de inicio de sesión correctos del usuario en el dominio, se debe consultar cada controlador de dominio del dominio y se debe usar la suma de los valores. Tenga en cuenta que el atributo no se replica, por lo que es posible que los controladores de dominio retirados también tengan recuento de inicios de sesión para el usuario y que falte en el recuento.

> [!IMPORTANT]
> Debido a la compatibilidad con versiones de 16 bits de LAN Manager, el atributo tiene un límite superior de 65535. Una vez alcanzado este límite, no se puede usar como indicador de la actividad del usuario en este controlador de dominio.

 

 

 





