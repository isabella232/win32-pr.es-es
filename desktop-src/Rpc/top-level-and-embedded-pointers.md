---
title: Top-Level y punteros incrustados
description: Para entender cómo se asignan los punteros y sus elementos de datos asociados en Microsoft RPC, debe diferenciar entre los punteros de nivel superior y los punteros incrustados.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486999"
---
# <a name="top-level-and-embedded-pointers"></a>Top-Level y punteros incrustados

Para entender cómo se asignan los punteros y sus elementos de datos asociados en Microsoft RPC, debe diferenciar entre los punteros de *nivel superior* y los *punteros incrustados*. También es útil hacer referencia al conjunto de todos los punteros que no son punteros de nivel superior.

Los *punteros de nivel superior* son aquellos que se especifican como nombres de parámetros en prototipos de función. Los punteros de nivel superior y sus correspondientes siempre se asignan en el servidor.

Los *punteros incrustados* son punteros que se incrustan en estructuras de datos como matrices, estructuras y uniones. Cuando los punteros incrustados solo escriben la salida en un búfer y son NULL en la entrada, la aplicación de servidor puede cambiar sus valores a un valor distinto de NULL. En este caso, el código auxiliar del cliente asigna memoria nueva para estos datos.

Si el puntero incrustado no es null en el cliente antes de la llamada, el código auxiliar no asigna memoria en el cliente en la devolución. En su lugar, el código auxiliar intenta escribir la memoria asociada al puntero incrustado en la memoria existente en el cliente asociado a ese puntero, sobrescribiendo los datos ya existentes.

> [!Note]  
> En el caso de los datos leídos o escritos en un búfer y que no especifica el tamaño del búfer, la longitud de salida debe ser menor o igual que la longitud de entrada. Se produce una excepción RPC cuando se detecta desbordamiento. En el caso de los datos de cadena, la longitud de salida se determina mediante la comprobación de la longitud de la cadena de entrada. Por lo tanto, las cadenas de salida no pueden superar la longitud de las cadenas de entrada. La guía de procedimientos recomendados es evitar esto al incluir siempre un parámetro especificado por el tamaño para indicar el tamaño del búfer.

 

Los punteros de solo escritura incrustados se tratan en [combinación de atributos direccionales y de puntero](combining-pointer-and-directional-attributes.md).

El término *punteros de nivel nontop* hace referencia a todos los punteros que no se especifican como nombres de parámetro en el prototipo de función, incluidos los punteros incrustados y varios niveles de punteros anidados.

 

 




