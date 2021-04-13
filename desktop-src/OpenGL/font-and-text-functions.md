---
title: Funciones de fuente y texto (OpenGL)
description: Las siguientes funciones se pueden usar para administrar fuentes y texto.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Funciones de WGL, texto
- Funciones de WGL, fuente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421817"
---
# <a name="font-and-text-functions-opengl"></a>Funciones de fuente y texto (OpenGL)

Las siguientes funciones se pueden usar para administrar fuentes y texto.



| Función de Windows                                 | Descripción                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | Crea un conjunto de listas de visualización de mapas de bits de caracteres. Los caracteres proceden de la fuente actual del contexto del dispositivo especificado. Los caracteres se especifican como una ejecución consecutiva en el conjunto de glifos de la fuente.                                      |
| [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | Crea un conjunto de listas de presentación, en función de los glifos de la fuente de contorno seleccionada actualmente de un contexto de dispositivo, para su uso con el contexto de representación actual. Las listas de visualización se utilizan para dibujar caracteres 3D de fuentes TrueType. |



 

Las funciones **wglUseFontBitmaps** y **wglUseFontOutlines** toman un identificador de un contexto de dispositivo y usan la fuente actual del contexto del dispositivo como origen de los mapas de bits. Por lo tanto, es necesario establecer la fuente del contexto del dispositivo y las propiedades de la fuente antes de llamar a **wglUseFontBitmaps** o **wglUseFontOutlines**.

Las funciones [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) y [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) también toman un parámetro que convierte el primer glifo de la fuente en una lista de visualización de mapa de bits y un parámetro que especifica el número de glifos que se van a convertir en listas de visualización. A continuación, la función crea listas de visualización para la ejecución consecutiva de glifos especificada. Por ejemplo:

-   Para crear un conjunto de listas de visualización de mapas de bits de 224 para todos los glifos de juego de caracteres de Windows, establezca estos dos parámetros en 32 y 224, respectivamente.
-   Para crear un conjunto de listas de visualización de mapas de bits de 256 para todos los glifos de juego de caracteres OEM, establezca estos dos parámetros en 0 y 256, respectivamente.
-   Para crear una lista de visualización de un solo mapa de bits para un glifo de un solo juego de caracteres, establezca el segundo de estos parámetros en 1.

Las funciones **wglUseFontBitmaps** y **wglUseFontOutlines** representan un glifo nulo en una fuente con una lista de visualización vacía.

Las listas de visualización creadas mediante una llamada a **wglUseFontBitmaps** o **wglUseFontOutlines** se numeran automáticamente de forma consecutiva.

Después de llamar a la función [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) o [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) , llame a [**glCallLists**](glcalllists.md) para dibujar una cadena de caracteres. Vea [dibujar texto en una Double-Buffered ventana de OpenGL](drawing-text-in-a-double-buffered-opengl-window.md) para ver el código de ejemplo. En este contexto, **glCallLists** usa cada carácter de una cadena como un índice en la matriz de listas de presentación numeradas de forma consecutiva creadas por **wglUseFontBitmaps** o **wglUseFontOutlines**.

Cuando termine de dibujar texto, llame a la función [**glDeleteLists**](gldeletelists.md) para liberar el conjunto contiguo de listas de presentación creadas por **wglUseFontBitmaps** y **wglUseFontOutlines**.

 

 




