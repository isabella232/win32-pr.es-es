---
description: 'Más información acerca de: estructura de JET_CONVERT'
title: Estructura de JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908258"
---
# <a name="jet_convert-structure"></a>Estructura de JET_CONVERT


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_convert-structure"></a>Estructura de JET_CONVERT

La estructura **JET_CONVERT** contiene el nombre de una DLL de la versión de ese anterior que se usa para leer las bases de datos que se crean con esa versión anterior. Además, se proporcionan otras marcas para controlar la naturaleza de la conversión.

**Windows Server 2003:** La característica de [JetCompact](./jetcompact-function.md) que realizó una conversión se ha quitado del producto en Windows Server 2003. Solo se admite en Windows 2000 y Windows XP.

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>Miembros

**SzOldDll**

El nombre, incluida la información de la ruta de acceso, a la versión anterior de la DLL de ESE.

**fFlags**

Reservado para uso del sistema.

**fSchemaChangesOnly**

Reservado para uso del sistema.

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
<td><p>Se implementa como <strong>JET_CONVERT_W</strong> (Unicode) y <strong>JET_CONVERT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetCompact](./jetcompact-function.md)
