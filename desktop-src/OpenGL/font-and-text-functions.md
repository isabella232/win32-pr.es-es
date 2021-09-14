---
title: Funciones de fuente y texto (OpenGL)
description: Las siguientes funciones se pueden usar para administrar fuentes y texto.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Funciones WGL,text
- Funciones WGL,font
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245030"
---
# <a name="font-and-text-functions-opengl"></a>Funciones de fuente y texto (OpenGL)

Las siguientes funciones se pueden usar para administrar fuentes y texto.



| Windows Función                                 | Descripción                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | Crea un conjunto de listas de visualización de mapa de bits de caracteres. Los caracteres proceden de la fuente actual del contexto de dispositivo especificado. Los caracteres se especifican como una ejecución consecutiva dentro del conjunto de glifos de la fuente.                                      |
| [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | Crea un conjunto de listas de visualización, basadas en los glifos de la fuente de esquema seleccionada actualmente de un contexto de dispositivo, para su uso con el contexto de representación actual. Las listas para mostrar se usan para dibujar caracteres 3D de fuentes TrueType. |



 

Las **funciones wglUseFontBitmaps** y **wglUseFontOutlines** toman un identificador para un contexto de dispositivo y usan la fuente actual de ese contexto de dispositivo como origen para los mapas de bits. Por lo tanto, es necesario establecer la fuente del contexto del dispositivo y las propiedades de la fuente antes de llamar a **wglUseFontBitmaps** o **wglUseFontOutlines.**

Las funciones [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) y [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) también toman un parámetro que convierte el primer glifo de la fuente en una lista de visualización de mapa de bits y un parámetro que especifica cuántos glifos se convertirán en listas de visualización. A continuación, la función crea listas de visualización para la ejecución consecutiva especificada de glifos. Por ejemplo:

-   Para crear un conjunto de 224 listas de visualización de mapa de bits para todos los glifos del juego de caracteres Windows, establezca estos dos parámetros en 32 y 224, respectivamente.
-   Para crear un conjunto de 256 listas de visualización de mapa de bits para todos los glifos de juego de caracteres oem, establezca estos dos parámetros en 0 y 256, respectivamente.
-   Para crear una lista de visualización de mapa de bits única para cualquier glifo de juego de caracteres único, establezca el segundo de estos parámetros en 1.

Las **funciones wglUseFontBitmaps** y **wglUseFontOutlines** representan un glifo null en una fuente con una lista de visualización vacía.

Las listas para mostrar creadas por una llamada a **wglUseFontBitmaps** o **wglUseFontOutlines** se numeran automáticamente de forma consecutiva.

Después de llamar a [**la función wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) o [**wglUseFontOutlines,**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) llame a [**glCallLists**](glcalllists.md) para dibujar una cadena de caracteres. Vea Drawing Text in a Double-Buffered OpenGL Window (Dibujar [texto en una ventana de OpenGL)](drawing-text-in-a-double-buffered-opengl-window.md) para obtener código de ejemplo. En este contexto, **glCallLists** usa cada carácter de una cadena como índice en la matriz de listas de visualización numeradas consecutivamente creadas por **wglUseFontBitmaps** o **wglUseFontOutlines.**

Cuando termine de dibujar texto, llame a la función [**glDeleteLists**](gldeletelists.md) para liberar el conjunto contiguo de listas de visualización creado por **wglUseFontBitmaps** y **wglUseFontOutlines.**

 

 




