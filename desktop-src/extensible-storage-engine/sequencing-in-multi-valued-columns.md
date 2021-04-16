---
description: Más información acerca de la secuenciación en columnas con varios valores
title: Secuenciación en columnas con varios valores
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553578"
---
# <a name="sequencing-in-multi-valued-columns"></a>Secuenciación en columnas con varios valores


_**Se aplica a:** Windows | Windows Server_

## <a name="sequencing-in-multi-valued-columns"></a>Secuenciación en columnas con varios valores

Los valores de una columna con varios valores se identifican mediante un número de índice denominado *itagSequence*. Este número es una referencia a un valor único de la columna. Este número se usa cuando se establecen, recuperan o enumeran nuevos valores en la columna. *ItagSequence* se utiliza en varias estructuras, entre las que se incluyen:

  - [JET_RETINFO](./jet-retinfo-structure.md)

  - [JET_SETINFO](./jet-setinfo-structure.md)

  - [JET_SETCOLUMN](./jet-setcolumn-structure.md)

  - [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)

  - [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)

Este *itagSequence* se inicia en 1 para cada valor de la columna con varios valores. El número de secuencia aumenta cuando se agregan nuevos valores a la columna. Al establecer un valor en una columna con un *itagSequence* de 0, se indica que el valor se va a anexar al conjunto de valores que ya se encuentra en esa columna. El uso de un valor de *itagSequence* mayor que el número de valores establecidos actualmente para una columna tendrá el mismo efecto. Si se especifica *itagSequence* de un valor existente, se sobrescribirá ese valor, no se insertará uno nuevo. Si se establece un valor existente en NULL, se quitará ese valor del conjunto de valores que ya se encuentra en esa columna. De esta forma, se desactivarán todos los valores subsiguientes de la columna en una ranura, de modo que el acceso posterior a esos valores por *itagSequence* estará en una cantidad inferior a la que se usó anteriormente.

En el diagrama siguiente se muestra un *itagSequence* en una columna con varios valores. La columna denominada ColA tiene tres entradas: Val1, Val2 y Val3 con *itagSequence* de 1, 2 y 3, respectivamente.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
