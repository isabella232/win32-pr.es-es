---
description: 'Más información acerca de: estructura de JET_RECSIZE2'
title: Estructura de JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
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
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706720"
---
# <a name="jet_recsize2-structure"></a>Estructura de JET_RECSIZE2


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_recsize2-structure"></a>Estructura de JET_RECSIZE2

[JetGetRecordSize2](./jetgetrecordsize2-function.md) utiliza la estructura de **JET_RECSIZE2** para devolver información sobre los requisitos de uso de un registro en el espacio de datos del usuario, el número de columnas establecidas, el número de valores y el espacio de sobrecarga de la estructura de los registros de ese.

**Windows 7:** La estructura de **JET_RECSIZE2** se introduce en el sistema operativo Windows 7.

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
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
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

**cCompressedColumns**

Número total de columnas comprimidas.

**cbDataCompressed**

Tamaño comprimido de los datos de usuario en este registro. Es lo mismo que cbData si no se comprimen valores largos intrínsecos.

**cbLongValueDataCompressed**

Tamaño comprimido de los datos de usuario en el árbol de valores largos. Esto es lo mismo que los datos de cbLongValue si no se comprimen valores largos separados.

### <a name="remarks"></a>Observaciones

El número total de valores del registro sería **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

Los datos lógicos del registro son (cbData + cbLongValueData) y el tamaño físico de los datos es (cbDataCompressed + cbLongValueDataCompressed). Se puede usar para calcular la razón de compresión de los datos almacenados.

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere el sistema operativo Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere el sistema operativo Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JetGetRecordSize](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
