---
description: 'Más información sobre: Columnas de valor largo'
title: Columnas de valor largo
TOCTitle: Long Value Columns
ms:assetid: 0690f9d3-1a58-4e53-92e1-213630fc88f4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269179(v=EXCHG.10)
ms:contentKeyID: 32765482
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: bb5618227d49de9e246adf69868a3cb2dc498dca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269644"
---
# <a name="long-value-columns"></a>Columnas de valor largo


_**Se aplica a:** Windows | Windows Servidor_

## <a name="long-value-columns"></a>Columnas de valor largo

Los tipos de columna ESE JET_coltypLongText y JET_coltypLongBinary se denominan tipos de columna de valor largo. Estas columnas son objetos binarios grandes y de cadena grande que se pueden almacenar en árboles B+ independientes lejos del índice principal. Cuando los valores largos se almacenan separados del registro principal, se claven internamente en un identificador de valor largo (LID) y un desplazamiento de bytes y se accede a ellos como una secuencia. Las columnas de valor largo se agregan a la tabla en la llamada a [JetAddColumn](./jetaddcolumn-function.md) con el miembro **coltyp** de la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) establecido en JET_coltypLongText o JET_coltypLongBinary. El tamaño máximo de un valor de columna Long Text o Long Binary es de 2 GB a 1.

ESE admite operaciones append, byte range overwrite y set size para columnas de valor largo para admitir implementaciones de flujo eficaces en estos tipos de columna. De forma predeterminada, los datos de valor largo se almacenan en un árbol B+ independiente si tienen más de 1024 bytes o si el registro no cabe en una sola página de base de datos cuando los datos de valor largo se almacenan en el registro. La aplicación tiene la opción de invalidar el comportamiento predeterminado estableciendo opciones para almacenar datos de valor largo en el registro (JET_bitSetIntrinsicLV) o para forzar su almacenamiento en el árbol B+ independiente (JET_bitSetIntrinsicLV). Estos valores se establecen en el parámetro *grbit* de [JetSetColumn](./jetsetcolumn-function.md)o el miembro **grbit** [JET_SETCOLUMN](./jet-setcolumn-structure.md) se usa en la llamada a [JetSetColumns](./jetsetcolumns-function.md) de la siguiente manera:

  - Anexar: (JET_bitSetAppendLV)

  - Sobrescritura del intervalo de bytes: (JET_bitSetOverwriteLV)

  - Establecer tamaño: (JET_bitSetSizeLV)

  - Forzar separación: (JET_bitSetSeparateLV)

  - Almacenar en el registro: (JET_bitSetIntrinsicLV)

Los datos de valor largo se establecen indicando el desplazamiento en el blob de valor largo y la longitud de los datos de valor largo en el blob. El desplazamiento al blob de valor largo se establece en el miembro **ibLongValue** de la estructura [JET_SETINFO](./jet-setinfo-structure.md) (para [JetSetColumn)](./jetsetcolumn-function.md)o en el miembro **ibLongValue** de la estructura [JET_SETCOLUMN](./jet-setcolumn-structure.md) (para [JetSetColumns).](./jetsetcolumns-function.md) El **miembro pvData** [de JET_SETCOLUMN](./jet-setcolumn-structure.md)y el parámetro *pvData* de la llamada a [JetSetColumn](./jetsetcolumn-function.md) contiene los datos de valor largo. Las actualizaciones de las columnas de valor largo deben realizarse dentro de una transacción.

Los datos de valor largo siempre se almacenan en una tabla independiente cuando la aplicación establece el JET_bitSetSeparateLV o JET_bitSetIntrinsicLV; de lo contrario, se decide de forma heurística. ESE almacena el valor largo separado si es mayor que 1024 bytes o si el registro no cabe en una sola página de base de datos si se almacena en el registro.

En el diagrama siguiente se muestran los datos de valor largo almacenados en una tabla independiente. Cuando se almacena un valor largo fuera del registro, se crea un nuevo identificador con valores largos para hacer referencia a su valor. Esto permite que varios registros haga referencia al mismo valor de columna. Los recuentos de referencia a los datos aumentan si más de un registro de los datos apunta a los mismos datos de valor largo.

![ESE_Documentation_longvaluedtree2](images/Gg269179.ESE_Documentation_longvaluedtree2(EXCHG.10).gif "ESE_Documentation_longvaluedtree2")

ESE también admite una característica de almacén de instancia única que permite que varios registros haga referencia al mismo objeto binario grande que si cada registro tuviera su propia copia de la información. evitando así copias duplicadas de los datos de valor de columna. Esta característica está habilitada en la llamada a [JetPrepareUpdate](./jetprepareupdate-function.md) con la JET_prepInsertCopy opción establecida en el *parámetro prep.*
