---
description: 'Más información sobre: JET_SIGNATURE estructura'
title: JET_SIGNATURE estructura
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: 9d254a392ade9daa43382d8418f2dda90729eddc81f6c3bbd7013d89ae8f2e74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616195"
---
# <a name="jet_signature-structure"></a>JET_SIGNATURE estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_signature-structure"></a>JET_SIGNATURE estructura

La **JET_SIGNATURE** contiene información que identifica de forma única una base de datos.

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a>Miembros

**ulRandom**

Número asignado aleatoriamente.

**logtimeCreate**

El [JET_LOGTIME](./jet-logtime-structure.md) en el momento de [ejecutar JetCreateDatabase.](./jetcreatedatabase-function.md)

**szComputerName**

Valor de cadena opcional del nombre NetBIOS del equipo. Este valor no se puede establecer.

### <a name="remarks"></a>Comentarios

Se puede encontrar como un elemento de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).

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
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)
