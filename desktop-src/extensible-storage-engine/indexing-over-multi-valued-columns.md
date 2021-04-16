---
description: 'Más información sobre: indexación en columnas multivalor'
title: Indexación de columnas con varios valores
TOCTitle: Indexing over Multi-Valued Columns
ms:assetid: 90e31df2-2f5b-47a8-84c1-ece6bcc40858
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269341(v=EXCHG.10)
ms:contentKeyID: 32765630
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: aea24e8423b704b7e0345898bcb6ae4b6d7c057b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696646"
---
# <a name="indexing-over-multi-valued-columns"></a>Indexación de columnas con varios valores


_**Se aplica a:** Windows | Windows Server_

## <a name="indexing-over-multi-valued-columns"></a>Indexación de columnas con varios valores

La indización en columnas con varios valores solo se realiza en la primera columna con varios valores del índice. La primera columna con varios valores se expande para que todos los valores de la columna se indexen. Todas las demás columnas con varios valores se indizan solo en el primer valor de la columna. Por ejemplo, un índice se define en la columna A y en la columna B, donde ambas columnas tienen varios valores. En un registro determinado, la columna A tiene los valores rojo y azul, y la columna B tiene los valores 1, 2 y 3. El índice resultante proporcionaría entradas para rojo-1 y azul-1. Los valores de la segunda columna, la columna B, no se expanden. Tenga en cuenta que, aunque cada columna etiquetada solo puede tener varios valores, las columnas etiquetadas explícitamente marcadas como de varios valores a través de JET_bitColumnMultiValued se expanden de esta manera. Además, debido al hecho de que las entradas de índice principal contienen registros, no se permite tener un índice principal en una columna con varios valores, ya que esto daría lugar a varias ubicaciones en el índice en el que tendría que residir el registro. Para obtener más información, vea el tema [columnas etiquetadas, fijas y de variables](./tagged-fixed-and-variable-columns.md) .

A partir de Windows Vista, los usuarios tienen la opción de establecer la opción JET_bitIndexCrossProduct cuando el índice se crea con [JetCreateIndex](./jetcreateindex-function.md) o [JetCreateIndex2](./jetcreateindex2-function.md) mediante la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) . Cuando se establece esta opción en un índice, se expanden todas las columnas de clave con varios valores del índice y se crea un producto cruzado en el índice para cada valor de esas columnas. El ejemplo anterior produce ahora entradas para rojo-1, rojo-2, rojo-3, azul-1, azul-2, azul-3. De nuevo, cada columna de clave se debe declarar explícitamente para que tenga varios valores a través de JET_bitColumnMultiValued para que se expanda en el índice.
