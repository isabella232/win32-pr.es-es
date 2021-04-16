---
description: 'Más información sobre: columnas dispersas con varios valores'
title: Columnas dispersas con varios valores
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21448d50e17881517086c1b258dcce02e84286a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716160"
---
# <a name="multi-valued-sparse-columns"></a>Columnas dispersas con varios valores


_**Se aplica a:** Windows | Windows Server_

## <a name="multi-valued-sparse-columns"></a>Columnas dispersas con varios valores

Las columnas dispersas pueden ser de longitud fija o variable, y son únicas en que no ocupan espacio en un registro si son NULL o están a la izquierda de su valor predeterminado. Las columnas dispersas, también denominadas columnas etiquetadas, pueden contener más de un valor en un solo registro. Las columnas etiquetadas pueden ser cualquiera de los tipos de columna descritos en las constantes de [JET_coltyp](./jet-coltyp.md) . Se crean cuando la columna se agrega a la tabla estableciendo la marca de JET_bitColumnTagged en la estructura de [JET_COLUMNDEF](./jet-columndef-structure.md) en la llamada a [JetAddColumn](./jetaddcolumn-function.md), o en la estructura [JET_COLUMNCREATE](./jet-columncreate-structure.md) utilizada en la llamada a [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) o [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). Las columnas de tipo JET_coltypLongText y JET_coltypLongBinary se crean automáticamente como columnas etiquetadas.

Solo las columnas etiquetadas pueden contener varios valores en un registro, las columnas de longitud fija o variable no pueden contener varios valores. Hay dos tipos de columnas con varios valores:

  - De forma predeterminada, las columnas etiquetadas tienen varios valores. Cuando se agrega un segundo valor a la columna, se convierte automáticamente en varios valores.

  - Columnas etiquetadas que se crean con la opción JET_bitColumnMultiValued en la estructura [JET_COLUMNDEF](./jet-columndef-structure.md) de la llamada a [JetAddColumn](./jetaddcolumn-function.md).

La opción JET_bitColumnMultiValued cambia la manera en que se indiza la columna. Las columnas con varios valores con la opción JET_bitColumnMultiValued se indizan de forma más exhaustiva que las columnas con varios valores etiquetados. Estas columnas se indizan en todos los valores de la columna con varios valores, mientras que las columnas con varios valores etiquetados solo se indexan sobre el primer valor de la columna con varios valores. Por ejemplo, considere una columna con varios valores en la que se establece la opción JET_bitColumnMultiValued y es la primera columna con varios valores de un índice. Esta columna contiene tres valores: A, B y C. Un índice sobre esta columna contiene entradas para los tres valores, A, B y C. Si no se ha establecido la opción JET_bitColumnMultiValued, el índice de esta columna solo contiene el primer valor, A, en el índice.
