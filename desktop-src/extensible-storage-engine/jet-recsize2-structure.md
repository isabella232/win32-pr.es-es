---
description: 'Más información sobre: JET_RECSIZE2 estructura'
title: JET_RECSIZE2 estructura
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
ms.openlocfilehash: c187d57149b7f0589d56439bfacbf7129ab4fe4a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987838"
---
# <a name="jet_recsize2-structure"></a>JET_RECSIZE2 estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_recsize2-structure"></a>JET_RECSIZE2 estructura

[JetGetRecordSize2](./jetgetrecordsize2-function.md) usa la estructura JET_RECSIZE2 para devolver información sobre los requisitos de uso de un registro en el espacio de datos del usuario, el número de columnas establecidas, el número de valores y el espacio de sobrecarga de la estructura de registro ese. 

**Windows 7:** La **JET_RECSIZE2** estructura se introduce en el sistema operativo Windows 7.

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

**cCompressedColumns**

Número total de columnas comprimidas.

**cbDataCompressed**

Tamaño comprimido de los datos de usuario de este registro. Esto es lo mismo que cbData si no se comprime ningún valor long intrínseco.

**cbLongValueDataCompressed**

Tamaño comprimido de los datos de usuario en el árbol de valor largo. Esto es lo mismo que los datos cbLongValue si no se comprime ningún valor long separado.

### <a name="remarks"></a>Observaciones

El número total de valores del registro sería **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.

Los datos lógicos del registro son (cbData+cbLongValueData) y el tamaño físico de los datos es (cbDataCompressed+cbLongValueDataCompressed). Se puede usar para calcular la proporción de compresión de los datos almacenados.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows sistema operativo Vista.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows sistema operativo Server 2008.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetGetRecordSize](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
