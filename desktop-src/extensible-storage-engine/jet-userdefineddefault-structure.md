---
description: 'Más información acerca de: estructura de JET_USERDEFINEDDEFAULT'
title: Estructura de JET_USERDEFINEDDEFAULT
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697674"
---
# <a name="jet_userdefineddefault-structure"></a>Estructura de JET_USERDEFINEDDEFAULT


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_userdefineddefault-structure"></a>Estructura de JET_USERDEFINEDDEFAULT

La estructura de **JET_USERDEFINEDDEFAULT** se especifica junto con JET_bitColumnUserDefinedDefault para asignar a una nueva columna un valor predeterminado que se determina mediante una devolución de llamada. Esta técnica se puede usar para implementar columnas calculadas.

**Windows XP:** La estructura de **JET_USERDEFINEDDEFAULT** se introduce en Windows XP.

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a>Miembros

**szCallback**

Nombre de exportación de la función que implementa la devolución de llamada en formato "función de módulo \! ".

La devolución de llamada se conserva como parte del esquema de columna. El ejecutable de host real y el nombre de exportación de la función deben persistir para habilitar la búsqueda de la dirección verdadera de la función en tiempo de ejecución.

El nombre del módulo es el nombre del archivo binario del host que contiene la función. El nombre de la función es el nombre de la exportación para esa función. El motor de base de datos utilizará estos dos fragmentos de información en tiempo de ejecución para localizar la dirección verdadera de la devolución de llamada mediante la ejecución de una llamada [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) en el nombre del módulo seguido de una llamada [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) en el nombre de la función.

Por ejemplo, si la devolución de llamada se implementó en un archivo DLL denominado MyCallback.DLL y ese archivo DLL se almacenó en C: myFunction \\ y la función que implementa la devolución de llamada se exportó desde el archivo dll como UserDefinedDefaultCallback, la cadena necesaria sería "C: myfunction \\ \\MyCallback.DLL\! UserDefinedDefaultCallback".

**Nota:**  Embedded " \! " no se admiten los caracteres de la parte del módulo del nombre de devolución de llamada.

Se recomienda encarecidamente que use un nombre de devolución de llamada que no sea una función de la arquitectura del host. Por ejemplo, no utilice exportaciones decoradas como Stdcall ( UserDefinedDefaultCallback@32 ) porque esta Convención de llamada solo se admite en equipos x86. Si se utilizara esta devolución de llamada, la base de datos solo podría usarse en un equipo x86. En este caso, se debe usar un alias para realizar una exportación independiente de la plataforma.

Se recomienda encarecidamente que use la ruta de acceso completa del nombre del módulo que implementa la devolución de llamada. Si se usa una ruta de acceso relativa, el proceso que hospeda la base de datos puede ser susceptible de sufrir ataques de un archivo binario no autorizado.

La aplicación solo debe pasar devoluciones de llamada de confianza al motor de base de datos. El motor de base de datos cargará el archivo binario para comprobar su existencia cuando se cree la columna asociada. Si la ruta de acceso al archivo binario no se valida o sabe que es de confianza, podría atacar el proceso que hospeda la base de datos.

**pbUserData**

Un bloque independiente de datos definidos por el usuario que se va a pasar a la devolución de llamada cuando se invoca. El bloque de datos que se proporciona se conservará como parte del esquema de columna. Como resultado, el bloque de datos debe ser completamente independiente y no puede hacer referencia a los datos que están fuera del ámbito de la base de datos.

Si **pbUserData** es cero, se omite el valor de **cbUserData** . En este caso, no se pasarán datos definidos por el usuario a la devolución de llamada cuando se invocan.

**cbUserData**

Vea **pbUserData**.

**szDependantColumns**

Reservado para uso futuro.

Este miembro siempre debe establecerse en NULL.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) y <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
