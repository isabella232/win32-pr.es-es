---
title: Acerca de las funciones de DrawDib
description: Acerca de las funciones de DrawDib
ms.assetid: 0ae993df-8393-479e-aa11-14301384715d
keywords:
- Vídeo para Windows (VFW), DrawDib
- VFW (vídeo para Windows), DrawDib
- DrawDib, acerca de
- DrawDib, tablas de color
- DrawDib, modo de transferencia
- DrawDib, adaptadores de pantalla
- DrawDib, ajuste de imagen
- DrawDib, imágenes comprimidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238f3e9ba822e16a7568775378b24f69bbca12de
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790881"
---
# <a name="about-the-drawdib-functions"></a>Acerca de las funciones de DrawDib

Colectivamente, las funciones de DrawDib son similares a la función [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) en cuanto a que proporcionan capacidades de ajuste de imagen y interpolación. Sin embargo, las funciones de DrawDib admiten la descompresión de imágenes, el streaming de datos y un mayor número de adaptadores de pantalla.

Le resultará útil usar las funciones de DrawDib en algunas circunstancias. Aun así, [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) es más diversa que las funciones de DrawDib y debe usarse cuando las funciones de DrawDib no pueden proporcionar la funcionalidad deseada. En la lista siguiente se describen los factores que se deben tener en cuenta a la hora de decidir si usar las funciones DrawDib o **StretchDIBits**.

-   Formato de información de tabla de colores. Las funciones DrawDib muestran imágenes que usan el formato de **\_ \_ colores RGB DIB** para su tabla de colores. Si las imágenes de la aplicación almacenan la información de la tabla de colores con los **\_ \_ colores DIB PAL** o el formato de **\_ \_ índices DIB PAL** , debe utilizar [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) para mostrarlas.
-   Modo de transferencia. Las funciones de DrawDib requieren que la aplicación use el modo de transferencia **SRCCOPY** . Si la aplicación usa [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) con un modo de transferencia distinto de **SRCCOPY**, debe seguir usando **StretchDIBits**. Del mismo modo, si necesita usar otras operaciones de trama en la aplicación, como XOR, use **StretchDIBits**.
-   Calidad de reproducción de vídeo y animación. Puede usar las funciones de DrawDib para las aplicaciones de streaming de datos, como las que reproducen clips de vídeo y secuencias animadas. Las funciones DrawDib superan [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) en cuanto a que proporcionan imágenes de mayor calidad y mejoran el movimiento durante la reproducción.
-   Adaptadores de pantalla. Las funciones DrawDib admiten un número mayor de adaptadores de pantalla que [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits) admite. Las funciones DrawDib admiten adaptadores de color VGA que proporcionan paletas de 16 colores con una profundidad de imagen de 4 bits, adaptadores SVGA que proporcionan paletas de 256 colores con una profundidad de imagen de 8 bits y adaptadores de pantalla de color verdadero que proporcionan miles de colores con profundidades de imagen de 16 bits, 24 bits y 32 bits.

    Las funciones de DrawDib también mejoran la velocidad y la calidad de la visualización de imágenes en adaptadores de pantalla con capacidades más limitadas. Por ejemplo, cuando se usa un adaptador de pantalla de 8 bits, DrawDib funciona de forma eficaz con una trama de imágenes de color verdadero a 256 colores. También traman imágenes de 8 bits al usar adaptadores de pantalla de 4 bits.

-   Ajuste de imagen. Al igual que [**StretchDIBits**](/windows/desktop/api/wingdi/nf-wingdi-stretchdibits), las funciones DrawDib usan rectángulos de origen y de destino para controlar la parte de una imagen que se muestra. Puede recortar partes no deseadas de una imagen o ajustar una imagen variando la posición y el tamaño de los rectángulos de origen y de destino. Si un controlador de pantalla no admite el ajuste de imagen, las funciones de DrawDib proporcionan funciones de ajuste más eficaces que **StretchDIBits**.
-   Imágenes comprimidas. Las funciones DrawDib dibujarán cualquier formato para el que tenga un descompresor, incluida la codificación de longitud de ejecución (RLE), Cinepak y 411 YUV. Windows incluye descompresores RLE y Cinepak que se pueden instalar opcionalmente.
-   El códec Indeo ya no se admite en Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DrawDib](drawdib.md)
</dt> </dl>

 

 