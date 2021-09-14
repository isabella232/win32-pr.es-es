---
title: Tessentar polígonos
description: Tessentar polígonos
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilidad OpenGL (GLU), teselación
- GLU (utilidad OpenGL), teselación
- Utilidad OpenGL (GLU), polígonos simples
- GLU (Utilidad OpenGL), polígonos simples
- Polígonos simples OpenGL
- Utilidad OpenGL (GLU), polígonos complejos
- GLU (utilidad OpenGL), polígonos complejos
- OpenGL de polígonos complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362009"
---
# <a name="tessellating-polygons"></a>Tessentar polígonos

OpenGL solo puede mostrar directamente polígonos convexas simples. Un polígono es simple si:

-   Los bordes solo se intersecan en los vértices.
-   No hay vértices duplicados.
-   Exactamente dos bordes se encuentran en cualquier vértice.

Para mostrar polígonos simples no convexas o polígonos simples que contengan huecos, primero debe triangular los polígonos (subdividirlos en polígonos convexas). Esta subdivisión se denomina *teselación*. GLU proporciona una colección de funciones que realizan teselación. Tenga en cuenta que las funciones de teselación de GLU no pueden controlar polígonos no simples; no hay ningún método OpenGL estándar para controlar estos polígonos.

Dado que la teselación suele ser necesaria y puede ser bastante complicada, en esta sección se describen las funciones de teselación de GLU en detalle. Estas funciones toman como entrada polígonos simples arbitrarios que pueden incluir huecos y devuelven alguna combinación de triángulos, mallas de triángulo y ventiladores de triángulo. Si no desea tratar con mallas o ventiladores, puede especificar que las funciones de teselación devuelvan solo triángulos. Sin embargo, la información de malla y ventilador mejora el rendimiento. Las funciones de teselación de polígonos triangulan un polígono cóncavo con uno o varios contornos.

**Para usar la teselación de polígonos**

1.  Cree un objeto de teselación [**con gluNewTess**](glunewtess.md).
2.  Use [*gluTessCallBack para*](glutess.md) definir las funciones de devolución de llamada que usará para procesar los triángulos generados por el teselador.
3.  Con [**gluBeginPolygon,**](glubeginpolygon.md) [**gluTessVertex,**](glutessvertex.md) [**gluNextContour**](glunextcontour.md)y [**gluEndPolygon,**](gluendpolygon.md)especifique el polígono con huecos o el polígono cóncavo que se va a teselar.

    Una vez completada la descripción del polígono, la instalación de teselación invoca las funciones de devolución de llamada según sea necesario.

    Puede destruir objetos de teselación innecesarios [**con gluDeleteTess**](gludeletetess.md).

Para obtener más información sobre cómo guardar los datos de teselación, vea [Usar funciones de devolución de llamada](using-callback-functions.md).

 

 




