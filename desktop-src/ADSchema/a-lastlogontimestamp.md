---
title: Atributo Last-Logon-Timestamp
description: Esta es la hora en que el usuario inició sesión por última vez en el dominio.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Last-Logon-Timestamp
- Esquema de AD del atributo lastLogonTimestamp
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaea56a7456a46b7583633992f77e6fd836276151e6c9f6b792ba1abdd36b4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322155"
---
# <a name="last-logon-timestamp-attribute"></a>Atributo Last-Logon-Timestamp

Esta es la hora en que el usuario inició sesión por última vez en el dominio. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). Cada vez que un usuario inicia sesión, el valor de este atributo se lee desde el controlador de dominio. Si el valor es \[ `current_time - msDS-LogonTimeSyncInterval` \] anterior, el valor se actualiza. La actualización inicial después del aumento del nivel funcional del dominio se calcula como 14 días menos el porcentaje aleatorio de 5 días.



| Entrada | Value |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| CN                | Marca de tiempo del último inicio de sesión                                                                                                   |
| Ldap-Display-Name | lastLogonTimestamp                                                                                                     |
| Size              | \-                                                                                                                     |
| Privilegio actualizar  | El sistema establece este valor.                                                                                       |
| Frecuencia de actualización  | Cuando el usuario inicia sesión, y si este valor es anterior a la hora actual menos el valor de msDS-LogonTimeSyncInterval. |
| Attribute-Id      | 1.2.840.113556.1.4.1696                                                                                                |
| System-Id-Guid    | c0e20a04-0e5a-4ff3-9482-5efeaecd7060                                                                                   |
| Syntax            | [**Intervalo**](s-interval.md)                                                                                         |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Falso                             |
| En el catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|-------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Verdadero                                                              |
| Es de un solo valor       | Verdadero                                                              |
| Está indexado             | Falso                                                             |
| En el catálogo global      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Clases usadas en        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Falso                             |
| En el catálogo global      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Verdadero                              |
| En el catálogo global      | Verdadero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Verdadero                              |
| En el catálogo global      | Verdadero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------|
| Id. de vínculo                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Es de un solo valor       | Verdadero                              |
| Está indexado             | Verdadero                              |
| En el catálogo global      | Verdadero                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



 

 





