---
title: Especificar devoluciones de llamada
description: Puede especificar hasta cinco funciones de devolución de llamada para una teselación.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilidad OpenGL (GLU), especificar funciones de devolución de llamada
- GLU (utilidad OpenGL), especificar funciones de devolución de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069265"
---
# <a name="specifying-callbacks"></a>Especificar devoluciones de llamada

Puede especificar hasta cinco funciones de devolución de llamada para una teselación. No se llama a las funciones que no especifique durante la teselación y no se obtiene ninguna información que puedan haber devuelto. Especifique las funciones de devolución de llamada [*con gluTessCallback*](glutess.md).

La **función gluTessCallback** asocia la función de devolución de llamada *fn* con el *objeto de teselación tessobj*. El tipo de devolución de llamada viene determinado por el tipo de parámetro *,* que puede ser **GLU \_ BEGIN,** **GLU EDGE \_ \_ FLAG,** **GLU \_ VERTEX,** **GLU \_ END** o **GLU \_ ERROR**. Las cinco funciones de devolución de llamada posibles tienen los siguientes prototipos.



| Función de devolución de llamada   | Prototipo                                    |
|---------------------|----------------------------------------------|
| **GLU \_ BEGIN**      | **void** **begin**(**tipo GLenum**_);_       |
| **MARCA \_ DE BORDE DE \_ GLU** | **void** **edgeFlag**(**marca GLboolean**_);_ |
| **VÉRTICE \_ DE GLU**     | **void** **vertex**(**void \* ,data* );     |
| **GLU \_ END**        | **void** **end**( *void* );                  |
| **ERROR DE GLU \_**      | **void** **error**(**GLenum**_errno_ );      |



 

Para cambiar una función de devolución de llamada, llame [*a gluTessCallback*](glutess.md) con la nueva función. Para eliminar una función de devolución de llamada sin reemplazarla por una nueva, pase **gluTessCallback** un puntero nulo para la función adecuada.

A medida que avanza la teselación, se llama a las funciones de devolución de llamada de una manera similar a la manera en que se usarían las funciones de OpenGL [**glBegin,**](glbegin.md) [glEdgeFlag,](gledgeflag-functions.md) [glVertex](glvertex-functions.md)y [**glEnd.**](glend.md)

La **función \_ de devolución** de llamada GLU BEGIN se invoca con uno de los tres parámetros posibles:

-   GL \_ TRIANGLE \_ FAN
-   FRANJA \_ DE TRIÁNGULO \_ GL
-   TRIÁNGULOS \_ GL

Después de llamar a la función de devolución de llamada **GLU \_ BEGIN** y antes de llamar a la función de devolución de llamada asociada a **GLU \_ END,** se invoca alguna combinación de las devoluciones de llamada **GLU EDGE \_ \_ FLAG** y **GLU \_ VERTEX.** Los vértices asociados y las marcas de borde se interpretan exactamente como están en OpenGL entre **glBegin**(GL \_ TRIANGLE \_ FAN), **glBegin**(GL TRIANGLE STRIP) o \_ \_ **glBegin**(GL \_ TRIANGLES) y el **glEnd correspondiente.**

Dado que las marcas de borde no tienen sentido en un ventilador de triángulo o una franja de triángulos, si hay una función de devolución de llamada asociada a **GLU \_ EDGE \_ FLAG**, la devolución de llamada **GLU \_ BEGIN** solo se llama con **GL \_ TRIANGLES**. La **función \_ de \_ devolución de** llamada GLU EDGE FLAG funciona de forma análoga a la función [glEdgeFlag de](gledgeflag-functions.md) OpenGL.

Si se produce un error durante la teselación, se invoca la función de devolución de llamada de error. A la función de devolución de llamada de error se le pasa un número de error glu. Puede obtener una cadena de caracteres que describa el error con la [**función gluErrorString.**](gluerrorstring.md)

 

 




