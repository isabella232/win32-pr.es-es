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
ms.openlocfilehash: 3a4d9500980434c21f9dfa6584db666418605de8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988618"
---
# <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_enumcolumnvalue-structure"></a>JET_ENUMCOLUMNVALUE estructura

La **JET_ENUMCOLUMNVALUE** enumera los valores de columna de un registro mediante la [función JetEnumerateColumns.](./jetenumeratecolumns-function.md) [JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de **JET_ENUMCOLUMNVALUE** estructuras. La matriz se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [reasignación](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a esa función.

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


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_wrnColumnNull</p> | <p>El valor de columna solicitado es NULL.</p> | 
| <p>JET_wrnColumnSkipped</p> | <p>La <em>itagSequence</em> que se especifica en el elemento de la <em>matriz rgtagSequence</em> en la estructura <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> correspondiente JET_ENUMCOLUMNVALUE <strong>estructura</strong> era cero.</p> | 
| <p>JET_wrnColumnTruncated</p> | <p>El valor de columna solicitado se truncaba al tamaño especificado antes de devolverse.</p><p>Este truncamiento solo se produce para columnas binarias largas y de texto largo que contienen grandes cantidades de datos.</p> | 



**cbData**

Valor de columna enumerado para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

**pvData**

Valor de columna enumerado para la columna.

El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada [compatible](/cpp/c-runtime-library/reference/realloc?view=vs-2019) con reasignación que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE]()  
[JET_ERR](./jet-err.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
