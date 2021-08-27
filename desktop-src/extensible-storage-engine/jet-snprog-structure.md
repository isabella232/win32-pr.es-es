---
description: 'Más información sobre: JET_SNPROG estructura'
title: JET_SNPROG estructura
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ab132d203ca2dc81e2ed3c3d8a0ce25c76a2cc71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987738"
---
# <a name="jet_snprog-structure"></a>JET_SNPROG estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_snprog-structure"></a>JET_SNPROG estructura

La **JET_SNPROG** estructura contiene información sobre el progreso de una operación de ejecución larga. Cuando se llama a la función de devolución de llamada para notificar el estado de la operación y la operación sigue en curso, el último parámetro de la función de devolución de llamada es un puntero a una **JET_SNPROG** estructura.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura **JET_SNPROG,** en bytes. Este valor confirma la presencia de los campos siguientes.

**cunitDone**

Número de unidades de trabajo que ya se han completado durante la función de larga duración.

**cunitTotal**

Número de unidades de trabajo que deben completarse. Este valor siempre debe ser mayor o igual que **cunitDone.**

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 


