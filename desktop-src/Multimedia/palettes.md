---
title: Las paletas
description: Las paletas
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- DrawDib, paletas
- DrawDibRealize función)
- DrawDibDraw función)
- DrawDibSetPalette función)
- DrawDibGetPalette función)
- DrawDibChangePalette función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5935831d8996c424a386f86082282f9cf7c1c12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995211"
---
# <a name="palettes"></a>Las paletas

Las funciones DrawDib requieren que una aplicación responda a dos mensajes orientados a la paleta: [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) y [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged). Si la aplicación no tiene en cuenta la paleta, tendrá que agregar un controlador para cada uno de estos mensajes. Para obtener más información sobre el procesamiento de los mensajes de **WM \_ QUERYNEWPALETTE** y **WM \_ PALETTECHANGED** , consulte [agregar controladores de mensajes de paleta](adding-palette-message-handlers.md).

Puede obtener la paleta DrawDib actual en el controlador de dominio mediante la función [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) . Debe obtener la paleta en respuesta al mensaje de [**\_ QUERYNEWPALETTE de WM**](/windows/desktop/gdi/wm-querynewpalette) o [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) , o bien al preparar la presentación de una secuencia de imagen mediante la función [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .

Puede dibujar una imagen asignada a otra paleta mediante la función [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) . Esta función obliga a que el controlador de dominio de DrawDib use la paleta especificada, lo que puede afectar a la calidad de la imagen. Por ejemplo, una aplicación que tenga en cuenta la paleta podría haber realizado una paleta y necesita evitar que DrawDib en su propia paleta. La aplicación puede utilizar **DrawDibSetPalette** para notificar a DrawDib de la paleta que se va a usar.

Puede obtener un identificador de la paleta de primer plano actual mediante la función [**DrawDibGetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) . Si la aplicación usa la paleta de primer plano actual, no tiene el uso exclusivo de la paleta y otra aplicación puede invalidar el identificador de la paleta. La aplicación no debe liberar la paleta cuando termine de usarla. La liberación de la paleta podría invalidar el identificador de la paleta para otra aplicación.

Puede preparar DrawDib para recibir nuevos valores de color para su paleta mediante la función [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) . En el código siguiente a **DrawDibChangePalette**, se asignan nuevos valores para la tabla de colores de la paleta. Si no se establece la marca de **\_ animación de DDF** en el controlador de dominio de DrawDib al llamar a **DrawDibChangePalette**, puede realizar los cambios de la paleta mediante [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para obtener la paleta. Después, puede usar [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para volver a dibujar la imagen. Si se establece la marca de **\_ animación de DDF** en el controlador de dominio DrawDib, puede animar la paleta y los colores del mapa de bits mostrado mediante **DrawDibDraw** o **DrawDibRealize**. Puede actualizar la marca **de \_ animación de DDF** mediante las funciones [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) y [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) .

> [!Note]  
> Si libera la paleta DrawDib mientras está seleccionada por un controlador de dominio, se puede producir un error de la interfaz de dispositivo gráfico (GDI) cuando el controlador de dominio use la paleta. En su lugar, la aplicación debe usar [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) para cambiar el controlador de dominio de DrawDib para que use la paleta predeterminada u otra paleta.

 

Las funciones [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend), [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)y [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) pueden liberar la paleta DrawDib. Sin embargo, estas funciones solo deben usarse cuando el controlador de dominio no ha seleccionado la paleta. La función DrawDibDraw también puede liberar la paleta cuando usa el mismo controlador de dominio DrawDib, pero especifica distintos parámetros de dibujo (*lpbi*, *dxDst*, *dyDst*, *dxSrc* o *dySrc*) o un formato diferente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de imágenes](image-rendering.md)
</dt> </dl>

 

 