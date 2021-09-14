---
description: 'Más información sobre: Columnas dispersas de varios valores'
title: Columnas dispersas de varios valores
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21448d50e17881517086c1b258dcce02e84286a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964200"
---
# <a name="multi-valued-sparse-columns"></a>Columnas dispersas de varios valores


_**Se aplica a:** Windows | Windows Servidor_

## <a name="multi-valued-sparse-columns"></a>Columnas dispersas de varios valores

Las columnas dispersas pueden tener una longitud fija o variable, y son únicas en que no ocupan espacio en un registro si son NULL o se quedan en su valor predeterminado. Las columnas dispersas, también denominadas columnas etiquetadas, pueden contener más de un valor en un único registro. Las columnas etiquetadas pueden ser cualquiera de los tipos de columnas que se describen en [JET_coltyp](./jet-coltyp.md) constantes. Se crean cuando la columna se agrega a la tabla estableciendo la marca JET_bitColumnTagged en la estructura JET_COLUMNDEF en la llamada [a](./jet-columndef-structure.md) [JetAddColumn](./jetaddcolumn-function.md)o en la estructura [JET_COLUMNCREATE](./jet-columncreate-structure.md) utilizada en la llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). Las columnas de tipo JET_coltypLongText y JET_coltypLongBinary automáticamente como columnas etiquetadas.

Solo las columnas etiquetadas pueden contener varios valores en un registro; es posible que las columnas de longitud fija o variable no contengan varios valores. Hay dos tipos de columnas multivalor:

  - Las columnas etiquetadas tienen varios valores de forma predeterminada. Cuando se agrega un segundo valor a la columna, se convierte automáticamente en multivalor.

  - Columnas etiquetadas que se crean con la JET_bitColumnMultiValued en [la JET_COLUMNDEF](./jet-columndef-structure.md) estructura en la llamada a [JetAddColumn](./jetaddcolumn-function.md).

La JET_bitColumnMultiValued cambia la forma en que se indexa la columna. Las columnas con varios valores con la JET_bitColumnMultiValued se indexan más ampliamente que las columnas de varios valores etiquetadas. Estas columnas se indexan sobre todos los valores de la columna con varios valores, mientras que las columnas con varios valores etiquetados solo se indexan sobre el primer valor de la columna con varios valores. Por ejemplo, considere una columna con varios valores en la que se JET_bitColumnMultiValued la opción y es la primera columna con varios valores en un índice. Esta columna contiene tres valores: A, B y C. Un índice sobre esta columna contiene entradas para los tres valores, A, B y C. Si no JET_bitColumnMultiValued la opción , el índice de esta columna solo contiene el primer valor, A, en el índice.
