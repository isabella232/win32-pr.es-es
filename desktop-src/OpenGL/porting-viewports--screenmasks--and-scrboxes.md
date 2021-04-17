---
title: Trasladar las ventanillas, Screenmasks y Scrboxes
description: Las siguientes funciones de ventanilla GL de IRIS no tienen ningún equivalente de OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Migración de GL de IRIS, funciones de ventanilla
- trasladar de IRIS GL, funciones de ventanilla
- trasladar a OpenGL desde IRIS GL, funciones de ventanilla
- Exportación de OpenGL desde IRIS GL, funciones de ventanilla
- funciones de ventanilla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665621"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>Trasladar las ventanillas, Screenmasks y Scrboxes

Las siguientes funciones de ventanilla GL de IRIS no tienen ningún equivalente de OpenGL:

-   **reshapeviewport**
-   **scrbox**
-   **getscrbox**

Con la función **VIEWPORT** GL de iris, se especifican las coordenadas x (en píxeles) de la izquierda y la derecha de un rectángulo de la ventanilla y las coordenadas y de la parte superior e inferior. Sin embargo, con la función [**glViewport**](glviewport.md) de OpenGL, se especifican las coordenadas x e y (en píxeles) de la esquina inferior izquierda del rectángulo de la ventanilla junto con el ancho y el alto.

En la tabla siguiente se enumeran las funciones de ventanilla GL de IRIS y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS                          | Función OpenGL                                                                                         | Significado                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **ventanilla** (izquierda, derecha, abajo, superior) | [**glViewport**](glviewport.md) (x, y, ancho y alto)                                                | Establece la ventanilla.           |
| **popviewportpushviewport**<br/>    | [**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) (bit de la ventanilla de contabilidad \_ \_ )<br/> | Envía y extrae la pila.   |
| **getviewport**                           | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (ventanilla de GL \_ )               | Devuelve las dimensiones de la ventanilla. |



 

??

 

 





