---
description: 'Más información acerca de: estructura de JET_SNPROG'
title: Estructura de JET_SNPROG
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
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496954"
---
# <a name="jet_snprog-structure"></a>Estructura de JET_SNPROG


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_snprog-structure"></a>Estructura de JET_SNPROG

La estructura **JET_SNPROG** contiene información sobre el progreso de una operación de ejecución prolongada. Cuando se llama a la función de devolución de llamada para notificar el estado de la operación y la operación aún está en curso, el último parámetro de la función de devolución de llamada es un puntero a una estructura de **JET_SNPROG** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño de la estructura de **JET_SNPROG** , en bytes. Este valor confirma la presencia de los campos siguientes.

**cunitDone**

El número de unidades de trabajo que ya se han completado durante la función de larga ejecución.

**cunitTotal**

El número de unidades de trabajo que se deben completar. Este valor siempre debe ser mayor o igual que **cunitDone**.

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
</tbody>
</table>

