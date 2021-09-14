---
title: Secuencias de imágenes
description: Secuencias de imágenes
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib,image sequences
- DrawDib, secuencia de mapas de bits
- Función DrawDibDraw
- Función DrawDibBegin
- Función DrawDibEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7ae2c85d62e93e4149518221aa520eabe13ee2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260839"
---
# <a name="sequences-of-images"></a>Secuencias de imágenes

Puede mostrar una secuencia de mapas de bits con las mismas dimensiones y formatos mediante la función [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) con la [**función DrawDibBegin.**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) **DrawDibBegin** mejora la eficacia de **DrawDibDraw** al preparar el controlador de dominio drawDib para dibujar.

> [!Note]  
> Si la aplicación no usa [**DrawDibBegin,**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) la ejecuta implícitamente antes de dibujar. Si la aplicación usa **DrawDibBegin** antes de **DrawDibDraw,** **DrawDibDraw** no tiene que procesar la función y esperar a que se complete.

 

La [**función DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) proporciona [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) con el controlador de dominio DrawDib, el controlador de dominio, la dirección de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) y las dimensiones del rectángulo de origen y destino. Cuando se muestra una secuencia de mapas de bits, **DrawDibDraw** comprueba los valores de estos elementos para cada imagen de la secuencia. Si **DrawDibDraw** detecta cambios en cualquiera de estos elementos, llama implícitamente a **DrawDibBegin** de nuevo para ajustar la configuración de DrawDib DC.

Después de [**usar DrawDibBegin,**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)puede dibujar la secuencia de imágenes mediante [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) y especificar una o varias marcas según corresponda. Especifique la **marca DDF \_ SAME \_ HDC** siempre y cuando el controlador de dominio no haya cambiado. Especifique la marca DDF SAME DRAW cuando los parámetros siguientes para \_ \_ **DrawDibDraw** no han cambiado: la dirección de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) y las dimensiones del rectángulo de origen y destino.

Puede actualizar las marcas establecidas con [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) mediante la función [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) seguida de otra llamada a **DrawDibBegin**. A **continuación, use DrawDibEnd para** borrar el controlador de dominio drawDib de sus marcas y configuraciones actuales. La llamada posterior **a DrawDibBegin** reinicializa el controlador de dominio drawDib con las marcas y la configuración adecuadas. Como alternativa, puede actualizar las marcas de un controlador de dominio DrawDib mediante **DrawDibBegin** sin **DrawDibEnd**. Para ello, debe cambiar al menos una de las siguientes configuraciones simultáneamente con las marcas: la dirección de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) o las dimensiones del rectángulo de origen o destino.

Puede aumentar la eficacia de [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para las operaciones de streaming de datos que usan imágenes comprimidas, como la reproducción de un clip de vídeo, mediante las funciones [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) y [**DrawDibStop.**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) La **función DrawDibStart** prepara el controlador de dominio drawDib para recibir una secuencia de imágenes mediante el envío de un mensaje al administrador de compresión de vídeo (VCM). Cuando el streaming ha finalizado, **DrawDibStop** envía un mensaje a VCM que indica que puede liberar los recursos que asignó para la operación de streaming de datos. Para obtener más información sobre VCM, vea [Administrador de compresión de vídeo](video-compression-manager.md).

> [!Note]  
> Debe especificar el ancho y el alto de los rectángulos de origen y destino en la aplicación. Sin embargo, no es necesario especificar los orígenes de los rectángulos. La aplicación puede volver a definir los orígenes de [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) para usar distintas partes de la imagen o para actualizar distintas partes de la pantalla.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de imágenes](image-rendering.md)
</dt> </dl>

 

 