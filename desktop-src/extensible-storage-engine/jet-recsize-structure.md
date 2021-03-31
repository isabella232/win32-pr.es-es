---
description: 'Más información acerca de: estructura de JET_RECSIZE'
title: Estructura de JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
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
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808540"
---
# <a name="jet_recsize-structure"></a>Estructura de JET_RECSIZE


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_recsize-structure"></a>Estructura de JET_RECSIZE

[JetGetRecordSize](./jetgetrecordsize-function.md) utiliza la estructura de **JET_RECSIZE** para devolver información sobre los requisitos de uso de un registro en el espacio de datos del usuario, el número de columnas establecidas, el número de valores y el espacio de sobrecarga de la estructura de los registros de ese.

**Windows Vista:** La estructura de **JET_RECSIZE** se introduce en Windows Vista.

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a>Miembros

**cbData**

Conjunto de datos de usuario en el registro.

**Nota:**  El tamaño de la clave no se incluye en este.

**cbLongValueData**

Datos de usuario asociados al registro pero almacenados en el árbol de valores largos.

**Nota:**  Esto no cuenta los valores largos intrínsecos.

**cbOverhead**

Sobrecarga de la estructura de registros de ESE para este registro. Esto incluye el tamaño de la clave del registro.

**cbLongValueOverhead**

Sobrecarga de los datos de valor largo.

**Nota:**  Esto no cuenta los valores largos intrínsecos.

**cNonTaggedColumns**

Número total de columnas fijas y variables establecidas en este registro.

**cTaggedColumns**

Número total de columnas etiquetadas establecidas en este registro.

**cLongValues**

Número total de valores Long almacenados en el árbol de valor largo para este registro.

**Nota:**  Esto no cuenta los valores largos intrínsecos.

**cMultiValues**

La acumulación del número total de valores más allá de la primera para todas las columnas del registro.

### <a name="remarks"></a>Observaciones

El número total de valores del registro sería **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetGetRecordSize](./jetgetrecordsize-function.md)
