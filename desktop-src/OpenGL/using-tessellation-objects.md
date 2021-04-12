---
title: Usar objetos de teselación
description: Como un polígono complejo se describe y se tesela, requiere datos asociados, como los vértices, los bordes y las funciones de devolución de llamada.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilidad OpenGL (GLU), objetos de teselación
- GLU (utilidad OpenGL), objetos de teselación
- objetos de teselación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356902"
---
# <a name="using-tessellation-objects"></a>Usar objetos de teselación

Como un polígono complejo se describe y se tesela, requiere datos asociados, como los vértices, los bordes y las funciones de devolución de llamada. Todos estos datos están asociados a un único objeto de teselación. Para dividirlas un polígono, primero se usa la función [**gluNewTess**](glunewtess.md) , que crea un nuevo objeto de teselación y devuelve un puntero a él. Si se produce un error en la función, se devuelve un puntero NULL.

Si ya no necesita un objeto de teselación, puede eliminarlo y liberar toda la memoria asociada con [**gluDeleteTess**](gludeletetess.md).

Puede reutilizar un solo objeto de teselación para todas las teselaciones. Este objeto solo es necesario porque las funciones de biblioteca pueden necesitar realizar sus propias teselaciones y deben poder hacerlo sin interferir con ninguna teselación que el programa esté realizando. Los objetos de teselación múltiples también son útiles si desea utilizar diferentes conjuntos de devoluciones de llamada para diferentes teselaciones. Sin embargo, normalmente se asigna un único objeto de teselación y se usa para todas las teselaciones. No hay ninguna necesidad real de liberarla, ya que utiliza una pequeña cantidad de memoria. Por otro lado, si está escribiendo una función de biblioteca que usa teselación GLU, tenga cuidado de liberar cualquier objeto de teselación que cree.

 

 




