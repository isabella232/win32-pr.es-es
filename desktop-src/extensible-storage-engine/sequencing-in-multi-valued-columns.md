---
description: 'Más información sobre: Secuenciación en columnas con varios valores'
title: Secuenciación en columnas con varios valores
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252681"
---
# <a name="sequencing-in-multi-valued-columns"></a>Secuenciación en columnas con varios valores


_**Se aplica a:** Windows | Windows Servidor_

## <a name="sequencing-in-multi-valued-columns"></a>Secuenciación en columnas con varios valores

Los valores de una columna con varios valores se identifican mediante un número de índice denominado *itagSequence*. Este número es una referencia a un único valor de la columna. Este número se usa cuando se establecen, recuperan o enumeran nuevos valores en la columna. La *itagSequence* se usa en varias estructuras, entre las que se incluyen:

  - [JET_RETINFO](./jet-retinfo-structure.md)

  - [JET_SETINFO](./jet-setinfo-structure.md)

  - [JET_SETCOLUMN](./jet-setcolumn-structure.md)

  - [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)

  - [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)

Esta *itagSequence* comienza en 1 para cada valor de la columna con varios valores. El número de secuencia aumenta cuando se agregan nuevos valores a la columna. Establecer un valor en una columna con una *itagSequence* de 0 indica que el valor se va a anexar al conjunto de valores que ya están en esa columna. El uso *de una itagSequence* mayor que el número de valores establecidos actualmente para una columna tendrá el mismo efecto. Si se especifica *la itagSequence* de un valor existente, se sobrescribirá ese valor, no se insertará uno nuevo. Si se establece un valor existente en NULL, se quitará ese valor del conjunto de valores que ya están en esa columna. Esto moverá todos los valores posteriores de la columna hacia abajo en una ranura, de modo que el acceso posterior a esos valores por *itagSequence* sea por un número uno menor que el que se usó anteriormente.

En el diagrama siguiente se *muestra una itagSequence* en una columna de varios valores. La columna denominada ColA tiene tres entradas: Val1, Val2 y Val3 con *itagSequence* de 1, 2 y 3 respectivamente.

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
