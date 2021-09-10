---
title: Acerca de las funciones DrawDib
description: Acerca de las funciones DrawDib
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- Vídeo para Windows (VFW),DrawDib
- VFW (vídeo para Windows),DrawDib
- DrawDib,about
- DrawDib, tablas de colores
- DrawDib, modo de transferencia
- DrawDib, adaptadores de pantalla
- DrawDib,image stretching
- DrawDib, imágenes comprimidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f3e9ba822e16a7568775378b24f69bbca12de
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371845"
---
# <a name="about-the-drawdib-functions"></a>Acerca de las funciones DrawDib

En conjunto, las funciones DrawDib son similares a la función [**StretchDIBits,**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) ya que proporcionan funcionalidades de extensión y dithering de imágenes. Sin embargo, las funciones DrawDib admiten la descompresión de imágenes, el streaming de datos y un mayor número de adaptadores de pantalla.

Le parecerá beneficioso usar las funciones DrawDib en algunas circunstancias. Aun así, [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) es más diverso que las funciones DrawDib y se debe usar cuando las funciones DrawDib no pueden proporcionar la funcionalidad deseada. En la lista siguiente se describen los factores que se deben tener en cuenta al decidir si se deben usar las funciones DrawDib o **StretchDIBits**.

-   Formato de información de tabla de colores. Las funciones DrawDib muestran imágenes que usan el formato **DIB \_ RGB \_ COLORS** para su tabla de colores. Si las imágenes de la tabla de colores del almacén de aplicaciones tienen el formato **DIB \_ PAL \_ COLORS** o **DIB \_ PAL \_ INDICES,** debe usar [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) para mostrarlas.
-   Modo de transferencia. Las funciones DrawDib requieren que la aplicación use el modo **de transferencia SRCCOPY.** Si la aplicación usa [**StretchDIBits con**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) un modo de transferencia distinto de **SRCCOPY,** debe seguir usando **StretchDIBits.** De forma similar, si necesita usar otras operaciones de trama en la aplicación, como XOR, use **StretchDIBits**.
-   Calidad de reproducción de vídeo y animación. Puede usar las funciones DrawDib para las aplicaciones de streaming de datos, como las que reproducen clips de vídeo y secuencias animadas. Las funciones DrawDib superan a [**StretchDIBits,**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) ya que proporcionan imágenes de mayor calidad y mejoran el movimiento durante la reproducción.
-   Adaptadores de pantalla. Las funciones DrawDib admiten un mayor número de adaptadores de pantalla que [**stretchDIBits.**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) Las funciones DrawDib admiten adaptadores de color VGA que proporcionan paletas de 16 colores mediante la profundidad de imagen de 4 bits, adaptadores SVGA que proporcionan paletas de 256 colores con profundidad de imagen de 8 bits y adaptadores de pantalla de color verdadero que proporcionan miles de colores mediante profundidades de imagen de 16 bits, 24 bits y 32 bits.

    Las funciones DrawDib también mejoran la velocidad y la calidad de la visualización de imágenes en adaptadores de pantalla con funcionalidades más limitadas. Por ejemplo, cuando se usa un adaptador de pantalla de 8 bits, DrawDib funciona de forma eficaz para difir imágenes de color verdadero a 256 colores. También incluyen otras imágenes de 8 bits cuando se usan adaptadores de pantalla de 4 bits.

-   Extensión de la imagen. Al [**igual que StretchDIBits,**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits)las funciones DrawDib usan rectángulos de origen y destino para controlar la parte de una imagen que se muestra. Puede recortar partes no deseadas de una imagen o extender una imagen variando la posición y el tamaño de los rectángulos de origen y destino. Si un controlador de pantalla no admite la extensión de imágenes, las funciones DrawDib proporcionan funcionalidades de stretching más eficaces que **StretchDIBits.**
-   Imágenes comprimidas. Las funciones DrawDib dibujarán cualquier formato para el que tenga un descomprimidor, incluida la codificación de longitud de ejecución (RLE), Cinecomposición y 411 YUV. Windows incluye descompresores de RLE y Cinecomposición que se pueden instalar opcionalmente.
-   El códec Indeo ya no se admite en Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DrawDib](drawdib.md)
</dt> </dl>

 

 