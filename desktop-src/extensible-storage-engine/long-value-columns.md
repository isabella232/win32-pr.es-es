---
description: 'Más información sobre: columnas de valor largo'
title: Columnas de valor largo
TOCTitle: Long Value Columns
ms:assetid: 0690f9d3-1a58-4e53-92e1-213630fc88f4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269179(v=EXCHG.10)
ms:contentKeyID: 32765482
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bb5618227d49de9e246adf69868a3cb2dc498dca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082026"
---
# <a name="long-value-columns"></a>Columnas de valor largo


_**Se aplica a:** Windows | Windows Server_

## <a name="long-value-columns"></a>Columnas de valor largo

Los tipos de columna ESE JET_coltypLongText y JET_coltypLongBinary se denominan tipos de columna de valor largo. Estas columnas son objetos grandes de cadena y binarios grandes que pueden almacenarse en árboles de B + independientes fuera del índice principal. Cuando se almacenan valores largos independientes del registro principal, se les asigna una clave interna con un identificador de valor largo (LID) y un desplazamiento de bytes, y se obtiene acceso a ellos como una secuencia. Las columnas de valor largo se agregan a la tabla en la llamada a [JetAddColumn](./jetaddcolumn-function.md) con el miembro **coltyp** de la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) establecida en JET_coltypLongText o JET_coltypLongBinary. El tamaño máximo de un valor de texto largo o de columna binaria larga es 2 GB-1.

ESE admite append, sobrescritura de intervalo de bytes y operaciones Set size para columnas de valor largo para admitir implementaciones de secuencias eficaces en estos tipos de columna. De forma predeterminada, los datos de valor largo se almacenan en un árbol B + independiente si es mayor que 1024 bytes, o si el registro no cabe en una sola página de base de datos cuando se almacenan los datos de valor largo en el registro. La aplicación tiene la opción de invalidar el comportamiento predeterminado estableciendo opciones para almacenar datos de valor largo en el registro (JET_bitSetIntrinsicLV) o para forzar que se almacenen en el árbol B + independiente (JET_bitSetIntrinsicLV). Estos valores se establecen en el parámetro *grbit* en [JetSetColumn](./jetsetcolumn-function.md), o bien el miembro **grbit** [JET_SETCOLUMN](./jet-setcolumn-structure.md) usar en la llamada a [JetSetColumns](./jetsetcolumns-function.md) como se indica a continuación:

  - Append: (JET_bitSetAppendLV)

  - Sobrescritura de intervalo de bytes: (JET_bitSetOverwriteLV)

  - Tamaño establecido: (JET_bitSetSizeLV)

  - Forzar independiente: (JET_bitSetSeparateLV)

  - Almacenar en registro: (JET_bitSetIntrinsicLV)

Los datos de valor largo se establecen indicando el desplazamiento en el BLOB de valor largo y la longitud de los datos de valor largo en el BLOB. El desplazamiento para el BLOB de valor largo se establece en el miembro **ibLongValue** de la estructura [JET_SETINFO](./jet-setinfo-structure.md) (para [JetSetColumn](./jetsetcolumn-function.md)) o el miembro **IbLongValue** de la estructura [JET_SETCOLUMN](./jet-setcolumn-structure.md) (para [JetSetColumns](./jetsetcolumns-function.md)). El miembro **pvData** de [JET_SETCOLUMN](./jet-setcolumn-structure.md)y el parámetro *PvData* de la llamada a [JetSetColumn](./jetsetcolumn-function.md) contiene los datos de valor largo. Las actualizaciones de las columnas de valor largo deben realizarse dentro de una transacción.

Los datos de valor largo siempre se almacenan en una tabla independiente cuando la aplicación establece el JET_bitSetSeparateLV o el JET_bitSetIntrinsicLV, de lo contrario se decide de forma heurística. ESE almacena el valor Long separado si es mayor que 1024 bytes o si el registro no cabe en una sola página de base de datos si se almacena en el registro.

En el diagrama siguiente se muestran los datos de valores largos almacenados en una tabla independiente. Cuando un valor largo se almacena fuera del registro, se crea un nuevo identificador de valor largo para hacer referencia a su valor. Esto permite que varios registros hagan referencia al mismo valor de columna. Los recuentos de referencias a los datos aumentan si más de un registro de los datos apunta a los mismos datos de valor largo.

![ESE_Documentation_longvaluedtree2](images/Gg269179.ESE_Documentation_longvaluedtree2(EXCHG.10).gif "ESE_Documentation_longvaluedtree2")

ESE también admite una característica de almacén de instancia única que permite que varios registros hagan referencia al mismo objeto binario grande como si cada registro tuviera su propia copia de la información. por lo tanto, se evitan las copias duplicadas de los datos de valores de columna. Esta característica está habilitada en la llamada a [JetPrepareUpdate](./jetprepareupdate-function.md) con la opción JET_prepInsertCopy establecida en el parámetro *Prep* .
