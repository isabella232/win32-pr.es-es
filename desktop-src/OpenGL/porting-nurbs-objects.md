---
title: Trasladar objetos de NURBS
description: OpenGL trata a NURBS como objetos, de forma similar al modo en que trata Quadrics crea un objeto NURBS y, a continuación, especifica cómo se debe representar. En la tabla siguiente se enumeran las funciones de OpenGL GLU para administrar objetos de NURBS.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Migración de GL de IRIS, objetos de NURBS
- portabilidad de IRIS GL, objetos de NURBS
- trasladar a OpenGL desde IRIS GL, objetos de NURBS
- Exportación de OpenGL desde IRIS GL, objetos de NURBS
- Objetos NURBS
- NURBS (no uniforme, B-spline racional)
- B-spline racional no uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418877"
---
# <a name="porting-nurbs-objects"></a>Trasladar objetos de NURBS

OpenGL trata a NURBS como objetos, de forma similar al modo en que trata Quadrics: se crea un objeto NURBS y, a continuación, se especifica cómo se debe representar. En la tabla siguiente se enumeran las funciones de OpenGL GLU para administrar objetos de NURBS.



| Función GLU de OpenGL                                      | Significado                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)       | Crea un nuevo objeto NURBS.                                    |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) | Elimina un objeto NURBS.                                        |
| [*gluNurbsCallback*](glunurbs.md)                       | Asocia una devolución de llamada a un objeto NURBS para el control de errores. |



 

Al migrar el código NURBS de GL de IRIS a OpenGL, tenga en cuenta los puntos siguientes:

-   Los puntos de control de NURBS son Float, no dobles.
-   El parámetro STRIDE se cuenta en Float, no en bytes.
-   Si usa la iluminación y no está especificando las normales, llame a [**glEnable**](glenable.md) con GL \_ auto \_ normal como parámetro para generar las normales automáticamente.

??

 

 




