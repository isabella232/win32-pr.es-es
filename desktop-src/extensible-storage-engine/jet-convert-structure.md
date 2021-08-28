---
description: 'Más información sobre: JET_CONVERT estructura'
title: JET_CONVERT estructura
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
ms.openlocfilehash: 804f76e274a04e4f1eff0b3b8de5b2ca8c3064a8aa9d915c3d2514da64f2eeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731115"
---
# <a name="jet_convert-structure"></a>JET_CONVERT estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_convert-structure"></a>JET_CONVERT estructura

La **JET_CONVERT** contiene el nombre de un archivo DLL de versión ese anterior que se usa para leer una base de datos creada con esa versión anterior. Además, se proporcionan otras marcas para controlar la naturaleza de la conversión.

**Windows Server 2003:** La característica de [JetCompact](./jetcompact-function.md) que realizó una conversión se quitó del producto en Windows Server 2003. Solo se admite en Windows 2000 y Windows XP.

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

Nombre, incluida la información de ruta de acceso, a la versión anterior del archivo DLL de ESE.

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
<td><p><strong>Servidor</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en Esent.h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JET_CONVERT_W</strong> (Unicode) <strong>y JET_CONVERT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetCompact](./jetcompact-function.md)
