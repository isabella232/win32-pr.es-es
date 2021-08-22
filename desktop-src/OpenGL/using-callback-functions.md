---
title: Usar funciones de devolución de llamada
description: Las funciones de devolución de llamada GLU, gluBeginPolygon, gluTessVertex, gluNextContour y gluEndPolygon, son similares a las funciones de polígono OpenGL.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- Utilidad OpenGL (GLU), funciones de devolución de llamada
- GLU (utilidad OpenGL), funciones de devolución de llamada
- Utilidad OpenGL (GLU), teselación
- GLU (utilidad OpenGL), teselación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75556b8c366c83df5a5976c867e6fc5f68d520da65ed8f34609f312cbfebaa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932900"
---
# <a name="using-callback-functions"></a>Usar funciones de devolución de llamada

Las funciones de devolución de llamada [**gluBeginPolygon,**](glubeginpolygon.md) [**gluTessVertex,**](glutessvertex.md) [**gluNextContour**](glunextcontour.md)y [**gluEndPolygon**](gluendpolygon.md)son similares a las funciones de polígono OpenGL.

Normalmente, guarda los datos de los triángulos, las mallas de triángulo y los ventiladores de triángulos en estructuras de datos definidas por el usuario o en listas de visualización openGL. Para representar los polígonos, otro código recorre las estructuras de datos o llama a las listas para mostrar. Aunque las funciones de devolución de llamada podrían llamar a funciones OpenGL para mostrar los polígonos directamente, esto no suele hacerse, ya que la teselación puede realizar un uso intensivo de recursos computacionalmente. Es una buena idea guardar los datos si hay alguna posibilidad de que quiera volver a mostrarlo. Se garantiza que las funciones de teselación GLU nunca devolverán nuevos vértices, por lo que nunca se requiere la interpolación de vértices, coordenadas de textura o colores.

 

 




