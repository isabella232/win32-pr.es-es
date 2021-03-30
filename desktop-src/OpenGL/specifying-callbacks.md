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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532415"
---
# <a name="specifying-callbacks"></a>Especificar devoluciones de llamada

Puede especificar hasta cinco funciones de devolución de llamada para una teselación. No se llama a las funciones que no se especifican durante la teselación y no se obtiene ninguna información que puedan haber devuelto. Las funciones de devolución de llamada se especifican con [*gluTessCallback*](glutess.md).

La función **gluTessCallback** asocia la función de devolución de llamada *FN* con el objeto de teselación *tessobj*. El tipo de la devolución de llamada viene determinado por el *tipo* de parámetro, que puede ser **Glu \_ Begin**, **Glu \_ Edge \_ Flag**, **Glu \_ Vertex**, **Glu \_ End** o **Glu \_ error**. Las cinco funciones de devolución de llamada posibles tienen los siguientes prototipos.



| Función de devolución de llamada   | Prototipo                                    |
|---------------------|----------------------------------------------|
| **Inicio de GLU \_**      | **void** **Begin**(**GLenum * ** *);       |
| **\_marca de borde Glu \_** | **void** **EdgeFlag**(**GLboolean ** * *); |
| **\_vértice Glu**     | **void** **Vertex**(**void \* * * * Data* );     |
| **final de GLU \_**        | **void** **End**( *void* );                  |
| **\_error Glu**      |  **error** void (**GLenum * * errno* );      |



 

Para cambiar una función de devolución de llamada, llame a [*gluTessCallback*](glutess.md) con la nueva función. Para eliminar una función de devolución de llamada sin reemplazarla por una nueva, pase **gluTessCallback** un puntero NULL para la función adecuada.

A medida que la teselación continúa, se llama a las funciones de devolución de llamada de forma similar a como se haría con las funciones de OpenGL [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md)y [**glEnd**](glend.md).

La función de devolución de llamada de **\_ Inicio Glu** se invoca con uno de los tres parámetros posibles:

-   \_ventilador de triángulo GL \_
-   \_franja de triángulo de GL \_
-   triángulos de contabilidad \_

Después de llamar a la función de devolución de llamada de **\_ Inicio de Glu** y antes de llamar a la función de devolución de llamada asociada al **\_ extremo de Glu**, se invoca una combinación de las devoluciones de llamada **\_ perimetral Glu \_** y **Glu \_ Vertex** . Los vértices asociados y las marcas de borde se interpretan exactamente como están en OpenGL entre **glBegin**(fan triangular GL \_ \_ ), **glBegin**(franja triangular de GL \_ \_ ) o **glBegin**( \_ triángulos de contabilidad **)** y la **glEnd** coincidente.

Dado que las marcas de borde no tienen sentido en un ventilador de triángulo o en una franja de triángulo, si hay una función de devolución de llamada asociada con la **\_ \_ marca de borde de Glu**, la devolución de llamada de **\_ Inicio de Glu** solo se llama con **\_ triángulos de contabilidad**. La función de devolución de llamada de **\_ \_ marcador perimetral Glu** funciona de forma análoga a la función [glEdgeFlag](gledgeflag-functions.md) de OpenGL.

Si se produce un error durante la teselación, se invoca la función de devolución de llamada de error. La función de devolución de llamada de error pasa un número de error GLU. Puede obtener una cadena de caracteres que describa el error con la función [**gluErrorString**](gluerrorstring.md) .

 

 




