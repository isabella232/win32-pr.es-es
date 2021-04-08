---
title: Especificar el polígono que se va a teselar
description: Se especifica un polígono (posiblemente con huecos) que se va a teselar mediante
ms.assetid: 23e56d3e-c26c-4158-b0ce-cf8fcea22927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff36b74f9484a76f938a7a24847c218f5c4e8dbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994545"
---
# <a name="specifying-the-polygon-to-be-tessellated"></a>Especificar el polígono que se va a teselar

Especifique un polígono (posiblemente con huecos) para que se pueda crear una teselación mediante:

-   [**gluBeginPolygon**](glubeginpolygon.md)
-   [**gluTessVertex**](glutessvertex.md)
-   [**gluNextContour**](glunextcontour.md)
-   [**gluEndPolygon**](gluendpolygon.md)

En el caso de los polígonos sin huecos, el proceso de especificación es exactamente como en OpenGL:

1.  Comience con [**gluBeginPolygon**](glubeginpolygon.md).
2.  Llame a [**gluTessVertex**](glutessvertex.md) para cada vértice del límite.
3.  Finalice el polígono con una llamada a [**gluEndPolygon**](gluendpolygon.md).

Si un polígono está compuesto de varios contornos, incluidos los huecos y los huecos dentro de los huecos, debe especificar los contornos uno detrás del otro, precedidos por [**gluNextContour**](glunextcontour.md). Cuando se llama a [**gluEndPolygon**](gluendpolygon.md), señala el final del contorno final e inicia la teselación. Puede omitir la llamada a **gluNextContour** antes del primer contorno. La función [**gluBeginPolygon**](glubeginpolygon.md) inicia la especificación de un polígono que se va a teselar y asocia un objeto de teselación, **tessobj**, con él. Las funciones de devolución de llamada que se van a usar son las que se enlazan al objeto de teselación con [*gluTessCallback*](glutess.md).

La función [**gluTessVertex**](glutessvertex.md) especifica un vértice en el polígono que se va a teselar. Llame a **gluTessVertex** para cada vértice del polígono. El parámetro *tessobj* de la función es el objeto de teselación que se va a usar, *v* contiene las coordenadas de vértices tridimensionales y los *datos* son un puntero arbitrario que se envía a la devolución de llamada asociada con el **\_ vértice Glu**. Normalmente, los *datos* contienen datos de vértices, coordenadas de textura, información de color o cualquier otra cosa que necesite la aplicación.

La función [**gluNextContour**](glunextcontour.md) marca el principio del siguiente contorno cuando varios contornos componen el límite del polígono para que sea teselado. El parámetro de *tipo* de la función puede ser **Glu \_ exterior**, **Glu \_ interior**, **Glu \_ CCW**, **Glu \_ CW** o **Glu \_ Unknown**. Estas constantes solo sirven como sugerencias para la teselación. Si los consigue, la teselación podría ir más rápida. Si los obtiene mal, se omiten y la teselación sigue funcionando.

En el caso de un polígono con huecos, un contorno es el contorno exterior y el otro es interior. Si no llama a **gluNextContour** inmediatamente después de [**gluBeginPolygon**](glubeginpolygon.md), se supone que el primer contorno es del tipo **Glu \_ exterior**.

**Glu \_ CW** y **Glu \_ CCW** indican polígonos orientados a la derecha y a las agujas del reloj. Elegir los que están en el sentido de las agujas del reloj y los que están en sentido contrario a las agujas del reloj son arbitrarios en tres dimensiones, pero en cualquier plano hay dos orientaciones diferentes; Use los tipos **Glu \_ CW** y **Glu \_ CCW** de forma coherente. Use **Glu \_ Unknown** si no sabe cuál usar.

La función [**gluEndPolygon**](gluendpolygon.md) indica el final de la especificación Polygon. También indica que la teselación puede empezar a usar el objeto de teselación *tessobj*.

 

 




