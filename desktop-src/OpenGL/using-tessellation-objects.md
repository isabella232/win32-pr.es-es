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
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073984"
---
# <a name="using-tessellation-objects"></a>Usar objetos de teselación

Como un polígono complejo se describe y se tesela, requiere datos asociados, como los vértices, los bordes y las funciones de devolución de llamada. Todos estos datos están vinculados a un único objeto de teselación. Para teselar un polígono, primero se usa la función [**gluNewTess,**](glunewtess.md) que crea un nuevo objeto de teselación y devuelve un puntero a él. Se devuelve un puntero nulo si se produce un error en la función.

Si ya no necesita un objeto de teselación, puede eliminarlo y liberar toda la memoria asociada con [**gluDeleteTess**](gludeletetess.md).

Puede reutilizar un único objeto de teselación para todas las teselaciones. Este objeto solo es necesario porque es posible que las funciones de biblioteca necesiten realizar sus propias teselaciones y deben poder hacerlo sin interferir con las teselaciones que el programa está realizando. Varios objetos de teselación también son útiles si desea usar diferentes conjuntos de devoluciones de llamada para diferentes teselaciones. Sin embargo, normalmente se asigna un único objeto de teselación y se usa para todas las teselaciones. No hay ninguna necesidad real de liberarla, porque usa una pequeña cantidad de memoria. Por otro lado, si está escribiendo una función de biblioteca que usa la teselación GLU, tenga cuidado de liberar los objetos de teselación que cree.

 

 




