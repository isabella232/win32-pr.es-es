---
title: Especificar el polígono que se va a teselar
description: Especifique un polígono (posiblemente que contenga huecos) que se va a teselar mediante
ms.assetid: 23e56d3e-c26c-4158-b0ce-cf8fcea22927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff36b74f9484a76f938a7a24847c218f5c4e8dbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161071"
---
# <a name="specifying-the-polygon-to-be-tessellated"></a>Especificar el polígono que se va a teselar

Especifique un polígono (posiblemente que contenga huecos) que se va a teselar mediante:

-   [**gluBeginPolygon**](glubeginpolygon.md)
-   [**gluTessVertex**](glutessvertex.md)
-   [**gluNextContour**](glunextcontour.md)
-   [**gluEndPolygon**](gluendpolygon.md)

En el caso de los polígonos sin huecos, el proceso de especificación es exactamente igual que en OpenGL:

1.  Comience con [**gluBeginPolygon.**](glubeginpolygon.md)
2.  Llame [**a gluTessVertex para**](glutessvertex.md) cada vértice del límite.
3.  Finalice el polígono con una llamada a [**gluEndPolygon.**](gluendpolygon.md)

Si un polígono consta de varios contornos, incluidos los huecos y los huecos dentro de los huecos, especifique los contornos uno tras otro, precediendo cada uno de [**ellos por gluNextContour**](glunextcontour.md). Cuando se llama [**a gluEndPolygon,**](gluendpolygon.md)indica el final del contorno final e inicia la teselación. Puede omitir la llamada a **gluNextContour antes** del primer contorno. La [**función gluBeginPolygon**](glubeginpolygon.md) comienza la especificación de un polígono que se va a teselar y asocia un objeto de teselación, **tessobj**, a él. Las funciones de devolución de llamada que se van a usar son las que se enlazan al objeto de teselación [*con gluTessCallback*](glutess.md).

La [**función gluTessVertex**](glutessvertex.md) especifica un vértice en el polígono que se va a teselar. Llame **a gluTessVertex para** cada vértice del polígono. El parámetro *tessobj* de la función es el objeto de teselación que se  va a usar, *v* contiene las coordenadas de vértice tridimensionales y los datos son un puntero arbitrario que se envía a la devolución de llamada asociada a **GLU \_ VERTEX.** Normalmente, *los datos contienen* datos de vértices, coordenadas de textura, información de color o cualquier otra cosa que requiera la aplicación.

La [**función gluNextContour**](glunextcontour.md) marca el principio del siguiente contorno cuando varios contornos son el límite del polígono que se va a teselar. El parámetro de tipo *de la* función puede ser **GLU \_ EXTERIOR,** **GLU \_ INTERIOR,** **GLU \_ CCW,** **GLU \_ CW** o **GLU \_ UNKNOWN.** Estas constantes solo sirven como sugerencias para la teselación. Si lo hace bien, la teselación puede ir más rápido. Si se equivocan, se omiten y la teselación sigue funcionando.

Para un polígono con huecos, un contorno es el contorno exterior y los demás son interiores. Si no llama a **gluNextContour** inmediatamente después de [**gluBeginPolygon**](glubeginpolygon.md), se supone que el primer contorno es de tipo **GLU \_ EXTERIOR.**

**GLU \_ CW** y **GLU \_ CCW** indican polígonos orientados a las agujas del reloj y en sentido contrario a las agujas del reloj. Elegir cuáles son en el sentido de las agujas del reloj y cuáles son en sentido contrario a las agujas del reloj es arbitrario en tres dimensiones, pero en cualquier plano hay dos orientaciones diferentes; use los **tipos GLU \_ CW** y **GLU \_ CCW** de forma coherente. Use **GLU \_ UNKNOWN** si no sabe cuál usar.

La [**función gluEndPolygon**](gluendpolygon.md) indica el final de la especificación del polígono. También indica que la teselación puede empezar a usar el objeto *de teselación tessobj*.

 

 




