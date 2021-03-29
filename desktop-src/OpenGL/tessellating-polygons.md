---
title: Teselar polígonos
description: Teselar polígonos
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilidad OpenGL (GLU), Teselación
- GLU (utilidad OpenGL), Teselación
- Utilidad OpenGL (GLU), polígonos simples
- GLU (utilidad OpenGL), polígonos simples
- polígonos sencillos OpenGL
- Utilidad OpenGL (GLU), polígonos complejos
- GLU (utilidad OpenGL), polígonos complejos
- polígonos complejos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665728"
---
# <a name="tessellating-polygons"></a>Teselar polígonos

OpenGL puede mostrar directamente solo polígonos convexo sencillos. Un polígono es sencillo si:

-   Los bordes solo se cruzan en los vértices.
-   No hay vértices duplicados.
-   Exactamente dos bordes se encuentran en cualquier vértice.

Para mostrar polígonos sencillos o polígonos simples que contienen huecos, primero debe triangular los polígonos (subdividirlos en polígonos convexa). Esta subdivisión se denomina *teselación*. GLU proporciona una colección de funciones que realizan la teselación. Tenga en cuenta que las funciones de teselación GLU no pueden controlar polígonos no simples; no hay ningún método OpenGL estándar para controlar estos polígonos.

Dado que la teselación suele ser necesaria y puede ser bastante complicada, en esta sección se describen en detalle las funciones de teselación GLU. Estas funciones toman como entrada polígonos simples arbitrarios que pueden incluir agujeros y devuelven una combinación de triángulos, mallas de triángulo y ventiladores de triángulo. Si no desea trabajar con mallas ni ventiladores, puede especificar que las funciones de teselación devuelvan solo triángulos. Sin embargo, la información de la malla y del ventilador mejora el rendimiento. Las funciones de teselación de polígonos triangulan un polígono cóncavo con uno o varios contornos.

**Para usar la teselación poligonal**

1.  Cree un objeto de teselación con [**gluNewTess**](glunewtess.md).
2.  Use [*gluTessCallBack*](glutess.md) para definir las funciones de devolución de llamada que se usarán para procesar los triángulos generados por del teselador.
3.  Con [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)y [**gluEndPolygon**](gluendpolygon.md), especifique el polígono con huecos o el polígono cóncavo que se va a teselar.

    Una vez completada la descripción del polígono, la utilidad de teselación invoca las funciones de devolución de llamada según sea necesario.

    Puede destruir objetos de teselación innecesarios con [**gluDeleteTess**](gludeletetess.md).

Para obtener más información sobre cómo guardar los datos de teselación, vea [usar funciones de devolución de llamada](using-callback-functions.md).

 

 




