---
title: Porte de ventanillas, máscaras de pantalla y scrboxes
description: Las siguientes funciones de ventanilla de IRIS GL no tienen equivalente openGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Porte de IRIS GL, funciones de ventanilla
- porte desde IRIS GL, funciones de ventanilla
- porte a OpenGL desde IRIS GL, funciones de ventanilla
- Porte de OpenGL desde IRIS GL, funciones de ventanilla
- funciones de ventanilla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362034"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>Porte de ventanillas, máscaras de pantalla y scrboxes

Las siguientes funciones de ventanilla de IRIS GL no tienen ningún equivalente openGL:

-   **reshapeviewport**
-   **scrbox**
-   **getscrbox**

Con la función de ventanilla **IRIS** GL, se especifican las coordenadas x (en píxeles) para la izquierda y la derecha de un rectángulo de ventanilla y las coordenadas y para la parte superior e inferior. Sin embargo, con la función [**glViewport**](glviewport.md) de OpenGL, se especifican las coordenadas x e y (en píxeles) de la esquina inferior izquierda del rectángulo de ventanilla junto con su ancho y alto.

En la tabla siguiente se enumeran las funciones de ventanilla DE IRIS GL y sus funciones OpenGL equivalentes.



| Función GL de IRIS                          | Función OpenGL                                                                                         | Significado                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **viewport** ( left, right, bottom, top ) | [**glViewport**](glviewport.md) ( x, y, width, height )                                                | Establece la ventanilla.           |
| **popviewportpushviewport**<br/>    | [**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL \_ VIEWPORT BIT \_ )<br/> | Inserta y abre la pila.   |
| **getviewport**                           | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ VIEWPORT )               | Devuelve dimensiones de ventanilla. |



 

??

 

 





