---
title: Procesamiento del vídeo
description: Procesamiento del vídeo
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Complementos de Windows Media Player, DSP de vídeo
- complementos, DSP de vídeo
- Complementos de procesamiento de señal digital, procesamiento de vídeo
- Complementos DSP, procesamiento de vídeo
- Complementos de DSP de vídeo, procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8d21aaa3999d05ea3628ff341c74379b07a6dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077934"
---
# <a name="processing-the-video"></a>Procesamiento del vídeo

Los detalles del vídeo de procesamiento varían en cada formato. queda fuera del ámbito de esta documentación proporcionar estos detalles. En un sentido general, el objetivo del complemento es cambiar los datos de color en el búfer de entrada y, a continuación, copiar los datos en el búfer de salida.

El complemento de ejemplo procesa dos tipos de formatos de vídeo: YUV y RGB.

En el caso de vídeo YUV, la información de color rojo y azul se codifica en los valores de ti y V y el nivel de luminancia se representa mediante el valor Y. el valor verde se codifica y se puede recuperar mediante un algoritmo. El complemento de ejemplo simplemente cambia los valores de ti y V para que afecten al nivel de color. Cada byte U o V tiene un valor entre cero y 255. En primer lugar, el complemento ajusta cada valor para que se represente en un intervalo de-128 a 127 y, a continuación, escala el valor por el factor de escala proporcionado. Por último, el código ajusta el valor de nuevo para el intervalo de cero a 255 original y copia los datos en el búfer de salida. En el código de ejemplo siguiente se procesa el vídeo UYVY. En este formato, cada otro byte es un valor U o Y.


```C++
while( dwHeight-- )
{
    DWORD x = dwWidth; 

        while( x-- )
        {
        // Scale the U and V bytes to 128.
        // Just copy the Y bytes.
        if( x%2 )
        {
            pbTarget[x] = pbSource[x];
        }
        else
        {
            long temp = (long)((pbSource[x] - 128) * m_fScaleFactor);

            // Truncate if exceeded full scale.
            if (temp > 127)
            temp = 127;
            if (temp < -128)
            temp = -128;

            pbTarget[x] = temp + 128;
        }
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



En el vídeo RGB, la información de color y luminancia se codifica como valores de rojo, verde y azul distintos. El complemento de ejemplo calcula el promedio de los tres valores para determinar el valor de Gray y, a continuación, ajusta cada valor de color mediante el factor de escala proporcionado. Una vez más, los valores se deben normalizar para el intervalo de-128 a 127 antes de la escala. El siguiente código de Process32Bit muestra el proceso de RGB32:


```C++
while( dwHeight-- )
{
    RGBQUAD* pPixelIn = (RGBQUAD*)pbSource;
    RGBQUAD* pPixelOut = (RGBQUAD*)pbTarget;

    for( DWORD x = 0; x < dwWidth; x++ )
    {
    // Get the color bytes.
    long lBlue = (long) pPixelIn[x].rgbBlue;
    long lGreen = (long) pPixelIn[x].rgbGreen;
    long lRed = (long) pPixelIn[x].rgbRed;

    // Compute the average for gray.
    long lAverage = ( lBlue + lGreen + lRed ) / 3;

    // Scale the colors to the average.
    pPixelOut[x].rgbBlue = (BYTE)( ( lBlue - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbGreen = (BYTE)( ( lGreen - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbRed = (BYTE)( ( lRed - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbReserved = pPixelIn[x].rgbReserved;
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



Para obtener más información acerca de los formatos de vídeo, consulte el [sitio web de FourCC](../directshow/fourcc-codes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento DSP de vídeo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 