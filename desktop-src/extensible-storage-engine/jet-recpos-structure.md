---
description: 'Más información sobre: JET_RECPOS structure'
title: JET_RECPOS estructura
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: ed374030bd3ab577b209d326d21110482c9cf37a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989118"
---
# <a name="jet_recpos-structure"></a>JET_RECPOS estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_recpos-structure"></a>JET_RECPOS estructura

La **JET_RECPOS** contiene una colección de enteros que representan una posición fraccionera dentro de un índice. **centriesLT es** el número de entradas de índice menor que la clave de índice actual. **centriesInRange es** el número de entradas de índice igual a la clave actual. **centriesInRange** no se admite y siempre se devuelve como 1. **centriesTotal es** el número de entradas de índice del índice. Todos los valores son aproximaciones sin garantía de precisión.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura [JET_RETINFO,](./jet-retinfo-structure.md) en bytes. Este valor confirma la presencia de los campos siguientes.

**centriesLT**

Número aproximado de entradas de índice menor que la clave actual.

**centriesInRange**

Número aproximado de entradas de índice igual a la clave actual. Este campo siempre se establece en 1, independientemente del número de entradas de índice que son realmente iguales a la clave actual.

**centriesTotal**

Número aproximado de entradas en el índice.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
