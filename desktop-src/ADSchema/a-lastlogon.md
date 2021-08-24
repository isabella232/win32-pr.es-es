---
title: Last-Logon atributo
description: La última vez que el usuario inició sesión.
ms.assetid: 271f4f38-90f9-4add-a3ed-413c224e1fae
ms.tgt_platform: multiple
keywords:
- Last-Logon esquema de AD del atributo
- Esquema de AD del atributo lastLogon
topic_type:
- apiref
api_name:
- Last-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe319611e9190d828e6ccb9abb4eea9e6b5675980dfb3ab7c143dcad8e7bc4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322215"
---
# <a name="last-logon-attribute"></a>Last-Logon atributo

La última vez que el usuario inició sesión. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). Un valor de cero significa que se desconoce la hora del último inicio de sesión.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Last-Logon                           |
| Ldap-Display-Name | lastLogon                            |
| Size              | 8 bytes                              |
| Privilegio actualizar  | El sistema establece este valor.     |
| Frecuencia de actualización  | Cada vez que el usuario inicia sesión.          |
| Attribute-Id      | 1.2.840.113556.1.4.52                |
| System-Id-Guid    | bf967997-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervalo**](s-interval.md)       |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
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
| System-Flags           | 0x00000011                        |
| Clases usadas en        | [**Usuario**](c-user.md)<br/> |



## <a name="remarks"></a>Comentarios

La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME.**

Este atributo no se replica y se mantiene por separado en cada controlador de dominio del dominio. Para obtener un valor preciso para el último inicio de sesión del usuario en el dominio, el atributo **Last-Logon** del usuario debe recuperarse de cada controlador de dominio del dominio. El valor más grande que se recupera es la hora de último inicio de sesión verdadera para ese usuario.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> </dl>

 

