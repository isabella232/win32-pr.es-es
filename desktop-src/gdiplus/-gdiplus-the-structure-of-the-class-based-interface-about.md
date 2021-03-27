---
description: La interfaz de C++ para Windows GDI+ contiene sobre las clases 40, las enumeraciones 50 y las 6 estructuras. También hay algunas funciones que no son miembros de ninguna clase.
ms.assetid: 46051bfa-b842-4e4e-bda8-e9003b5b5da4
title: Estructura de la interfaz basada en clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2627d695330c316a57c2593e75233d73b27a1524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997237"
---
# <a name="the-structure-of-the-class-based-interface"></a>Estructura de la interfaz basada en clases

La interfaz de C++ para Windows GDI+ contiene sobre las clases 40, las enumeraciones 50 y las 6 estructuras. También hay algunas funciones que no son miembros de ninguna clase.

Debe indicar que el espacio de nombres gdiplus se usa antes de que se llame a cualquier función de GDI+. La siguiente instrucción indica que el espacio de nombres gdiplus se usa en la aplicación.

`using namespace Gdiplus;`

La clase de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) es el núcleo de la interfaz GDI+; es la clase que, en realidad, dibuja líneas, curvas, figuras, imágenes y texto.

Muchas clases funcionan junto con la clase de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Por ejemplo, el método [Graphics::D rawline](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) recibe un puntero a un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , que contiene los atributos (color, ancho, guion y estilo like) de la línea que se va a dibujar. El método [Graphics:: FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) puede recibir un puntero a un objeto [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) , que funciona con el objeto **Graphics** para rellenar un rectángulo con un color que cambia gradualmente. Los objetos [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) y [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) influyen en la forma en que un objeto **Graphics** dibuja texto. Un objeto [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) almacena y manipula la transformación universal de un objeto **Graphics** , que se utiliza para girar, escalar y voltear imágenes.

Ciertas clases sirven principalmente como tipos de datos estructurados. Algunas de esas clases (por ejemplo, [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect), [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)y [**size**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-size)) son para fines generales. Otras son para fines especializados y se consideran clases auxiliares. Por ejemplo, la clase [**BitmapData**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-bitmapdata) es una aplicación auxiliar para la clase [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) y la clase [**PathData**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pathdata) es una aplicación auxiliar para la clase [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . GDI+ también define algunas estructuras que se usan para organizar los datos. Por ejemplo, la estructura [**colormap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) contiene un par de objetos de [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) que forman una entrada en una tabla de conversión de colores.

GDI+ define varias enumeraciones, que son colecciones de constantes relacionadas. Por ejemplo, la enumeración [**LineJoin**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin) contiene los [elementos * * * * LineJoinBevel * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin), * * * [* LineJoinMiter * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* y [* * * * LineJoinRound * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-linejoin)* *, que especifican estilos que se pueden usar para combinar dos líneas.

GDI+ proporciona algunas funciones que no forman parte de ninguna clase. Dos de esas funciones son [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) y [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). Debe llamar a **GdiplusStartup** antes de realizar cualquier otra llamada de GDI+ y debe llamar a **GdiplusShutdown** cuando haya terminado de usar GDI+.

 

 
