---
title: Paletas
description: Paletas
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- DrawDib,palettes
- Función DrawDibRealize
- Función DrawDibDraw
- Función DrawDibSetPalette
- Función DrawDibGetPalette
- Función DrawDibChangePalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5935831d8996c424a386f86082282f9cf7c1c12
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372452"
---
# <a name="palettes"></a>Paletas

Las funciones DrawDib requieren que una aplicación responda a dos mensajes orientados a la paleta: [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) y [**WM \_ PALETTECHANGED.**](/windows/desktop/gdi/wm-palettechanged) Si la aplicación no tiene en cuenta la paleta, deberá agregar un controlador para cada uno de estos mensajes. Para obtener más información sobre cómo procesar los **mensajes WM \_ QUERYNEWPALETTE** y **WM \_ PALETTECHANGED,** vea [Adding Palette Message Handlers](adding-palette-message-handlers.md).

Puede realizar la paleta DrawDib actual en el controlador de dominio mediante la [**función DrawDibRealize.**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) Debe darse cuenta de la paleta en respuesta al mensaje [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) o [**WM \_ PALETTECHANGED,**](/windows/desktop/gdi/wm-palettechanged) o al prepararse para mostrar una secuencia de imágenes mediante la función [**DrawDibDraw.**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw)

Puede dibujar una imagen asignada a otra paleta mediante la [**función DrawDibSetPalette.**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) Esta función obliga al controlador de dominio DrawDib a usar la paleta especificada, lo que puede afectar a la calidad de la imagen. Por ejemplo, una aplicación que tenga en cuenta la paleta podría haber realizado una paleta y debe impedir que DrawDib se dé cuenta de su propia paleta. La aplicación puede usar **DrawDibSetPalette para** notificar a DrawDib la paleta que se debe usar.

Puede obtener un identificador de la paleta de primer plano actual mediante la [**función DrawDibGetPalette.**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) Si la aplicación usa la paleta de primer plano actual, no tiene un uso exclusivo de la paleta y otra aplicación puede invalidar el identificador de la paleta. La aplicación no debe liberar la paleta cuando termine de usarlo. Liberar la paleta podría invalidar el identificador de la paleta para otra aplicación.

Puede preparar DrawDib para recibir nuevos valores de color para su paleta mediante la [**función DrawDibChangePalette.**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) En el código siguiente **a DrawDibChangePalette,** se asignan nuevos valores para la tabla de colores de la paleta. Si la marca **DDF \_ ANIMATE** no se establece en el controlador de dominio DrawDib al llamar a **DrawDibChangePalette,** puede aplicar los cambios de la paleta mediante [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) para realizar la paleta. A continuación, [**puede usar DrawDibDraw para**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) volver a dibujar la imagen. Si la **marca DDF \_ ANIMATE** está establecida en el controlador de dominio DrawDib, puede animar la paleta y los colores del mapa de bits mostrado mediante **DrawDibDraw** o **DrawDibRealize**. Puede actualizar la marca **DDF \_ ANIMATE** mediante las funciones [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) [**y DrawDibBegin.**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)

> [!Note]  
> Si libera la paleta DrawDib mientras está seleccionada por un controlador de dominio, se puede producir un error de interfaz de dispositivo gráfico (GDI) cuando el controlador de dominio usa la paleta. En su lugar, la aplicación debe usar [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) para cambiar el controlador de dominio drawDib para usar la paleta predeterminada u otra paleta.

 

Las [**funciones DrawDibEnd,**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)y [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) pueden liberar la paleta DrawDib. Sin embargo, estas funciones solo se deben usar cuando el controlador de dominio no haya seleccionado la paleta. La función DrawDibDraw también puede liberar la paleta cuando usa el mismo controlador de dominio DrawDib, pero especifica distintos parámetros de dibujo *(lpbi,* *dxDst,* *dyDst,* *dxSrc* o *dySrc)* o un formato diferente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de imágenes](image-rendering.md)
</dt> </dl>

 

 