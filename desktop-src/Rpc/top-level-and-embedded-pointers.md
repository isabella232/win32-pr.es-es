---
title: Top-Level punteros incrustados
description: Para entender cómo se asignan los punteros y sus elementos de datos asociados en RPC de Microsoft, debe diferenciar entre punteros de nivel superior y punteros incrustados.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f28fab18cfb345587f4c152f6890d94c5177e5bd9344e542592c33e462915beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011273"
---
# <a name="top-level-and-embedded-pointers"></a>Top-Level punteros incrustados

Para entender cómo se asignan los punteros y sus elementos de datos asociados en RPC de Microsoft, debe diferenciar entre *punteros* de nivel superior y *punteros incrustados.* También resulta útil hacer referencia al conjunto de todos los punteros que no son punteros de nivel superior.

*Los punteros de nivel* superior son los que se especifican como nombres de parámetros en prototipos de función. Los punteros de nivel superior y sus referenciadores siempre se asignan en el servidor.

*Los punteros incrustados* son punteros que se incrustan en estructuras de datos, como matrices, estructuras y uniones. Cuando los punteros incrustados solo escriben la salida en un búfer y son NULL en la entrada, la aplicación de servidor puede cambiar sus valores a distintos de NULL. En este caso, los códigos auxiliares de cliente asignan nueva memoria para estos datos.

Si el puntero incrustado no es NULL en el cliente antes de la llamada, los códigos auxiliares no asignan memoria al cliente en la devolución. En su lugar, el código auxiliar intenta escribir la memoria asociada al puntero incrustado en la memoria existente en el cliente asociado a ese puntero, sobrescribiendo los datos que ya están allí.

> [!Note]  
> Para los datos leídos o escritos en un búfer y que no especifican el tamaño del búfer, la longitud de salida debe ser menor o igual que la longitud de entrada. Cuando se detecta un desbordamiento, se produce una excepción RPC. Para los datos de cadena, la longitud de salida se determina mediante la comprobación de la longitud de la cadena de entrada. Por lo tanto, las cadenas de salida no pueden superar la longitud de las cadenas de entrada. La guía de procedimientos recomendados es evitarlo siempre incluyendo un parámetro de tamaño especificado para indicar el tamaño del búfer.

 

Los punteros de solo escritura insertados se de abordan [en Combinación de puntero y atributos direccionales.](combining-pointer-and-directional-attributes.md)

El término punteros de nivel no superior hace referencia a todos los *punteros* que no se especifican como nombres de parámetro en el prototipo de función, incluidos los punteros incrustados y varios niveles de punteros anidados.

 

 




