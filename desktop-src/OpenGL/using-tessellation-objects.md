---
title: Usar objetos de teselación
description: Como un polígono complejo se describe y se tesela, requiere datos asociados, como los vértices, los bordes y las funciones de devolución de llamada.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilidad OpenGL (GLU), objetos de teselación
- GLU (utilidad OpenGL), objetos de teselación
- Objetos de teselación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc2ca11fd037f79a88fed1568c97a24692060d723327cde0c8e8842ed21d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011903"
---
# <a name="using-tessellation-objects"></a>Usar objetos de teselación

Como un polígono complejo se describe y se tesela, requiere datos asociados, como los vértices, los bordes y las funciones de devolución de llamada. Todos estos datos están vinculados a un único objeto de teselación. Para teselar un polígono, primero se usa la función [**gluNewTess,**](glunewtess.md) que crea un nuevo objeto de teselación y devuelve un puntero a él. Se devuelve un puntero nulo si se produce un error en la función.

Si ya no necesita un objeto de teselación, puede eliminarlo y liberar toda la memoria asociada con [**gluDeleteTess**](gludeletetess.md).

Puede reutilizar un único objeto de teselación para todas las teselaciones. Este objeto solo es necesario porque es posible que las funciones de biblioteca necesiten realizar sus propias teselaciones, y deben ser capaces de hacerlo sin interferir con la teselación que el programa está realizando. Varios objetos de teselación también son útiles si desea usar diferentes conjuntos de devoluciones de llamada para diferentes teselaciones. Sin embargo, normalmente se asigna un único objeto de teselación y se usa para todas las teselaciones. No hay ninguna necesidad real de liberarla, ya que usa una pequeña cantidad de memoria. Por otro lado, si está escribiendo una función de biblioteca que usa teselación GLU, tenga cuidado de liberar los objetos de teselación que cree.

 

 




