---
title: Secuencias de imágenes
description: Secuencias de imágenes
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib, secuencias de imagen
- DrawDib, secuencia de mapas de bits
- DrawDibDraw función)
- DrawDibBegin función)
- DrawDibEnd función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7ae2c85d62e93e4149518221aa520eabe13ee2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665796"
---
# <a name="sequences-of-images"></a>Secuencias de imágenes

Puede mostrar una secuencia de mapas de bits con las mismas dimensiones y formatos mediante la función [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) con la función [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) . **DrawDibBegin** mejora la eficacia de **DrawDibDraw** al preparar el controlador de dominio de DrawDib para el dibujo.

> [!Note]  
> Si la aplicación no usa [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) la ejecuta implícitamente antes del dibujo. Si la aplicación usa **DrawDibBegin** antes de **DrawDibDraw**, **DrawDibDraw** no tiene que procesar la función y esperar a que se complete.

 

La función [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) proporciona [**DRAWDIBDRAW**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) con DrawDib DC, el identificador de DC, la dirección de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) y las dimensiones de rectángulo de origen y de destino. Cuando se muestra una secuencia de mapas de bits, **DrawDibDraw** comprueba los valores de estos elementos para cada imagen de la secuencia. Si **DrawDibDraw** detecta cambios en cualquiera de estos elementos, llama implícitamente a **DrawDibBegin** para ajustar la configuración del controlador de dominio de DrawDib.

Después de usar [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), puede dibujar la secuencia de imagen mediante [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) y especificar una o más marcas según corresponda. Especifique la marca DDF de la **\_ misma \_ HDC** siempre que el identificador del controlador de dominio no haya cambiado. Especifique la \_ misma marca de dibujo de DDF \_ cuando no hayan cambiado los siguientes parámetros para **DrawDibDraw** : la dirección de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) y las dimensiones del rectángulo de origen y de destino.

Puede actualizar las marcas establecidas con [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) mediante la función [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) seguida de otra llamada a **DrawDibBegin**. A continuación, use **DrawDibEnd** para borrar el controlador de dominio DrawDib de sus marcas y valores de configuración actuales. La siguiente llamada a **DrawDibBegin** reinicializa el controlador de dominio de DrawDib con las marcas y configuraciones adecuadas. Como alternativa, puede actualizar las marcas de un controlador de dominio de DrawDib mediante **DrawDibBegin** sin **DrawDibEnd**. Para ello, debe cambiar al menos una de las siguientes opciones simultáneamente con las marcas: la dirección de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) o las dimensiones del rectángulo de origen o de destino.

Puede aumentar la eficacia de [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para las operaciones de streaming de datos que usan imágenes comprimidas, como la reproducción de un clip de vídeo, mediante el uso de las funciones [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) y [**DrawDibStop**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) . La función **DrawDibStart** prepara el controlador de dominio de DrawDib para recibir un flujo de imágenes mediante el envío de un mensaje al administrador de compresión de vídeo (VCM). Cuando ha finalizado la transmisión por secuencias, **DrawDibStop** envía un mensaje a VCM que indica que puede liberar los recursos asignados para la operación de transmisión de datos. Para obtener más información sobre VCM, consulte [Administrador de compresión de vídeo](video-compression-manager.md).

> [!Note]  
> Debe especificar el ancho y el alto de los rectángulos de origen y de destino en la aplicación. Sin embargo, no es necesario especificar los orígenes de los rectángulos. La aplicación puede volver a definir los orígenes de [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para que usen distintas partes de la imagen o para actualizar distintas partes de la pantalla.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de imágenes](image-rendering.md)
</dt> </dl>

 

 