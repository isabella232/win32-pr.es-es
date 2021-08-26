---
description: 'Más información sobre: JET_ENUMCOLUMNVALUE estructura'
title: JET_ENUMCOLUMNVALUE estructura
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: 86905d49bb798d37bad48087c48e77349ec10f57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482291"
---
# <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE estructura

La **JET_ENUMCOLUMNVALUE** enumera los valores de columna de un registro mediante la [función JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de **JET_ENUMCOLUMNVALUE** estructuras. La matriz se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [el](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación que se proporcionó a esa función.

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a>Miembros

**itagSequence**

Valor de columna (por índice basado en uno) que se enumeró.

**Err**

Código de estado de columna resultante de la enumeración del valor de columna.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_wrnColumnNull</p> | <p>El valor de columna solicitado es NULL.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p>La <em>itagSequence</em> que se especifica en el elemento de la <em>matriz rgtagSequence</em> en la estructura <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> correspondiente JET_ENUMCOLUMNVALUE <strong>struct</strong> era cero.</p> | 
| <p>JET_wrnColumnTruncated</p> | <p>El valor de columna solicitado se truncaba al tamaño especificado antes de devolverse.</p><p>Este truncamiento solo se produce para columnas de texto largo y largas binarias que contienen grandes cantidades de datos.</p> | 



**cbData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en la memoria que se asignó mediante la devolución de llamada compatible con [la](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación que se proporcionó a [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

**pvData**

Valor de columna que se enumeró para la columna.

El búfer de salida se devuelve en la memoria que se asignó mediante la devolución de llamada compatible con [la](/cpp/c-runtime-library/reference/realloc?view=vs-2019) reasignación que se proporcionó a [JetEnumerateColumns.](./jetenumeratecolumns-function.md)

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
