---
description: 'Más información sobre: Columnas dispersas de varios valores'
title: Columnas dispersas de varios valores
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21dbe18be8be26af9fe32d9b80cbd5744c172793e27701d46438df4d63dcf395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115585"
---
# <a name="multi-valued-sparse-columns"></a>Columnas dispersas de varios valores


_**Se aplica a:** Windows | Windows Servidor_

## <a name="multi-valued-sparse-columns"></a>Columnas dispersas de varios valores

Las columnas dispersas pueden tener una longitud fija o variable, y son únicas en que no ocupan espacio en un registro si son NULL o se quedan en su valor predeterminado. Las columnas dispersas, también denominadas columnas etiquetadas, pueden contener más de un valor en un único registro. Las columnas etiquetadas pueden ser cualquiera de los tipos de columnas que se describen en [las JET_coltyp](./jet-coltyp.md) constantes. Se crean cuando la columna se agrega a la tabla estableciendo la marca JET_bitColumnTagged en la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) en la llamada a [JetAddColumn](./jetaddcolumn-function.md)o en la estructura [JET_COLUMNCREATE](./jet-columncreate-structure.md) utilizada en la llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). Las columnas de tipo JET_coltypLongText y JET_coltypLongBinary se crean automáticamente como columnas etiquetadas.

Solo las columnas etiquetadas pueden contener varios valores en un registro; es posible que las columnas de longitud fija o variable no contengan varios valores. Hay dos tipos de columnas multivalor:

  - Las columnas etiquetadas tienen varios valores de forma predeterminada. Cuando se agrega un segundo valor a la columna, se convierte automáticamente en multivalor.

  - Columnas etiquetadas que se crean con la JET_bitColumnMultiValued en [la JET_COLUMNDEF](./jet-columndef-structure.md) estructura en la llamada a [JetAddColumn](./jetaddcolumn-function.md).

La JET_bitColumnMultiValued cambia la forma en que se indexa la columna. Las columnas con varios valores con la JET_bitColumnMultiValued se indexan más ampliamente que las columnas con varios valores etiquetadas. Estas columnas se indexan sobre todos los valores de la columna con varios valores, mientras que las columnas con varios valores etiquetados solo se indexan sobre el primer valor de la columna con varios valores. Por ejemplo, considere una columna de varios valores donde se establece la opción JET_bitColumnMultiValued y es la primera columna de varios valores de un índice. Esta columna contiene tres valores: A, B y C. Un índice sobre esta columna contiene entradas para los tres valores, A, B y C. Si la JET_bitColumnMultiValued no se estableció, el índice de esta columna solo contiene el primer valor, A, en el índice.
