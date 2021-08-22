---
title: Acerca de las funciones DrawDib
description: Acerca de las funciones DrawDib
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- Vídeo para Windows (VFW),DrawDib
- VFW (vídeo para Windows),DrawDib
- DrawDib,about
- DrawDib, tablas de color
- DrawDib, modo de transferencia
- DrawDib, adaptadores de pantalla
- DrawDib, stretching de imagen
- DrawDib, imágenes comprimidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e03b41d5af776c39f7d100e9478bd408011d61d8e3d661cb80bd9ab52f08c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942093"
---
# <a name="about-the-drawdib-functions"></a>Acerca de las funciones DrawDib

Colectivamente, las funciones DrawDib son similares a la función [**StretchDIBits,**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) ya que proporcionan funcionalidades de extensión y dithering de imágenes. Sin embargo, las funciones DrawDib admiten la descompresión de imágenes, el streaming de datos y un mayor número de adaptadores de pantalla.

Le parecerá beneficioso usar las funciones DrawDib en algunas circunstancias. Aun así, [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) es más diverso que las funciones DrawDib y se debe usar cuando las funciones DrawDib no pueden proporcionar la funcionalidad deseada. En la lista siguiente se describen los factores que se deben tener en cuenta a la hora de decidir si se deben usar las funciones DrawDib o **StretchDIBits.**

-   Formato de información de tabla de colores. Las funciones DrawDib muestran imágenes que usan el formato **DIB \_ RGB \_ COLORS** para su tabla de colores. Si las imágenes de la tabla de colores del almacén de aplicaciones tienen el formato **DIB \_ PAL \_ COLORS** o **DIB \_ PAL \_ INDICES,** debe usar [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) para mostrarlas.
-   Modo de transferencia. Las funciones DrawDib requieren que la aplicación use el modo de **transferencia SRCCOPY.** Si la aplicación usa [**StretchDIBits con**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) un modo de transferencia distinto de **SRCCOPY,** debe seguir usando **StretchDIBits.** Del mismo modo, si necesita usar otras operaciones de trama en la aplicación, como XOR, use **StretchDIBits**.
-   Calidad de reproducción de vídeo y animación. Puede usar las funciones DrawDib para aplicaciones de streaming de datos, como las que reproducen clips de vídeo y secuencias animadas. Las funciones DrawDib superan a [**StretchDIBits,**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) ya que proporcionan imágenes de mayor calidad y mejoran el movimiento durante la reproducción.
-   Adaptadores de pantalla. Las funciones DrawDib admiten un mayor número de adaptadores de pantalla que [**los que admite StretchDIBits.**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) Las funciones DrawDib admiten adaptadores de color VGA que proporcionan paletas de 16 colores con una profundidad de imagen de 4 bits, adaptadores SVGA que proporcionan paletas de 256 colores con una profundidad de imagen de 8 bits y adaptadores de visualización de color verdadero que proporcionan miles de colores mediante profundidades de imagen de 16 bits, 24 bits y 32 bits.

    Las funciones DrawDib también mejoran la velocidad y la calidad de la visualización de imágenes en adaptadores de pantalla con funcionalidades más limitadas. Por ejemplo, cuando se usa un adaptador de pantalla de 8 bits, DrawDib funciona de forma eficaz para difir imágenes de color verdadero a 256 colores. También se difigen imágenes de 8 bits cuando se usan adaptadores de pantalla de 4 bits.

-   Extensión de la imagen. Al [**igual que StretchDIBits,**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)las funciones DrawDib usan rectángulos de origen y destino para controlar la parte de una imagen que se muestra. Puede recortar partes no deseadas de una imagen o extender una imagen variando la posición y el tamaño de los rectángulos de origen y destino. Si un controlador de pantalla no admite la extensión de imágenes, las funciones DrawDib proporcionan funcionalidades de extensión más eficaces que **StretchDIBits.**
-   Imágenes comprimidas. Las funciones DrawDib dibujarán cualquier formato para el que tenga un descompresión, incluida la codificación de longitud de ejecución (RLE), Cine ascii y 411 YUV. Windows incluye descompresores de RLE y Cinecomposición que se pueden instalar opcionalmente.
-   El códec Indeo ya no se admite en Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DrawDib](drawdib.md)
</dt> </dl>

 

 