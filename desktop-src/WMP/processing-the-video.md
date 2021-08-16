---
title: Procesamiento del vídeo
description: Procesamiento del vídeo
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Reproductor de Windows Media complementos, DSP de vídeo
- complementos, DSP de vídeo
- complementos de procesamiento de señales digitales, procesamiento de vídeo
- Complementos de DSP, procesamiento de vídeo
- complementos de DSP de vídeo, procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea168199270cfe8029b7b9303a7745db2c255f4268252a5bd80472a73c6f2f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334028"
---
# <a name="processing-the-video"></a>Procesamiento del vídeo

Los detalles del procesamiento de vídeo varían para cada formato; está fuera del ámbito de esta documentación para proporcionar estos detalles. En un sentido general, el objetivo del complemento es cambiar los datos de color en el búfer de entrada y, a continuación, copiar los datos en el búfer de salida.

El complemento de ejemplo procesa dos tipos de formatos de vídeo: YUV y RGB.

En el caso del vídeo YUV, la información de color rojo y azul se codifica en los valores you y V y el nivel de luminosidad se representa mediante el valor Y; el valor verde está codificado y se puede recuperar mediante un algoritmo. El complemento de ejemplo simplemente cambia los valores de you y V para que afecten al nivel de color. Cada byte U o V tiene un valor entre cero y 255. El complemento ajusta primero cada valor para que se represente mediante un intervalo de -128 a 127 y, a continuación, escala el valor por el factor de escala proporcionado. Por último, el código vuelve a ajustar el valor para el intervalo de cero a 255 original y copia los datos en el búfer de salida. El código de ejemplo siguiente procesa el vídeo UYVY. En este formato, todos los demás bytes son un valor U o Y.


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



En el caso del vídeo RGB, la información de color y luminosidad se codifica como valores rojos, verdes y azules independientes. El complemento de ejemplo calcula el promedio de los tres valores para determinar el valor del gris y, a continuación, ajusta cada valor de color mediante el factor de escala proporcionado. Una vez más, los valores deben normalizarse para el intervalo de -128 a 127 antes del escalado. El código siguiente de Process32Bit muestra el proceso para RGB32:


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



Para más información sobre los formatos de vídeo, consulte el [sitio web de FourCC.](../directshow/fourcc-codes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento DSP de vídeo**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 