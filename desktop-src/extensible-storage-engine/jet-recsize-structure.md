---
description: 'Más información sobre: JET_RECSIZE estructura'
title: JET_RECSIZE estructura
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
ms.openlocfilehash: 4fd0f59c821fa80d8de46f97e05aa1944354018e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475951"
---
# <a name="jet_recsize-structure"></a>JET_RECSIZE estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_recsize-structure"></a>JET_RECSIZE estructura

[JetGetRecordSize](./jetgetrecordsize-function.md) **usa** la estructura de JET_RECSIZE para devolver información sobre los requisitos de uso de un registro en el espacio de datos del usuario, el número de columnas establecidas, el número de valores y el espacio de sobrecarga de la estructura de registro ese.

**Windows Vista:** La **JET_RECSIZE** estructura se introduce en Windows Vista.

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

**Nota**  El tamaño de clave no se incluye en esto.

**cbLongValueData**

Datos de usuario asociados al registro pero almacenados en el árbol de valores largos.

**Nota**  Esto no cuenta los valores long intrínsecos.

**cbOverhead**

Sobrecarga de la estructura de registros ese para este registro. Esto incluye el tamaño de clave del registro.

**cbLongValueOverhead**

Sobrecarga de los datos de valor largo.

**Nota**  Esto no cuenta los valores long intrínsecos.

**cNonTaggedColumns**

Número total de columnas fijas y variables establecidas en este registro.

**cTaggedColumns**

Número total de columnas etiquetadas establecidas en este registro.

**cLongValues**

Número total de valores long almacenados en el árbol de valores largos para este registro.

**Nota**  Esto no cuenta los valores long intrínsecos.

**cMultiValues**

Acumulación del número total de valores más allá de la primera para todas las columnas del registro.

### <a name="remarks"></a>Comentarios

El número total de valores del registro sería **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetGetRecordSize](./jetgetrecordsize-function.md)
