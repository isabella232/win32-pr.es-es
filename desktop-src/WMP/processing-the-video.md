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
# <a name="processing-the-video"></a><span data-ttu-id="25966-108">Procesamiento del vídeo</span><span class="sxs-lookup"><span data-stu-id="25966-108">Processing the Video</span></span>

<span data-ttu-id="25966-109">Los detalles del vídeo de procesamiento varían en cada formato. queda fuera del ámbito de esta documentación proporcionar estos detalles.</span><span class="sxs-lookup"><span data-stu-id="25966-109">The details of processing video vary for each format; it is beyond the scope of this documentation to provide these details.</span></span> <span data-ttu-id="25966-110">En un sentido general, el objetivo del complemento es cambiar los datos de color en el búfer de entrada y, a continuación, copiar los datos en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="25966-110">In a general sense, the goal of the plug-in is to change the color data in the input buffer and then copy the data to the output buffer.</span></span>

<span data-ttu-id="25966-111">El complemento de ejemplo procesa dos tipos de formatos de vídeo: YUV y RGB.</span><span class="sxs-lookup"><span data-stu-id="25966-111">The sample plug-in processes two types of video formats: YUV and RGB.</span></span>

<span data-ttu-id="25966-112">En el caso de vídeo YUV, la información de color rojo y azul se codifica en los valores de ti y V y el nivel de luminancia se representa mediante el valor Y. el valor verde se codifica y se puede recuperar mediante un algoritmo.</span><span class="sxs-lookup"><span data-stu-id="25966-112">For YUV video, the red and blue color information is encoded in the U and V values and the luminance level is represented by the Y value; the green value is encoded and can be recovered by using an algorithm.</span></span> <span data-ttu-id="25966-113">El complemento de ejemplo simplemente cambia los valores de ti y V para que afecten al nivel de color.</span><span class="sxs-lookup"><span data-stu-id="25966-113">The sample plug-in simply changes the U and V values to affect the color level.</span></span> <span data-ttu-id="25966-114">Cada byte U o V tiene un valor entre cero y 255.</span><span class="sxs-lookup"><span data-stu-id="25966-114">Each U or V byte has a value between zero and 255.</span></span> <span data-ttu-id="25966-115">En primer lugar, el complemento ajusta cada valor para que se represente en un intervalo de-128 a 127 y, a continuación, escala el valor por el factor de escala proporcionado.</span><span class="sxs-lookup"><span data-stu-id="25966-115">The plug-in first adjusts each value to be represented by a range from -128 to 127, and then scales the value by the supplied scale factor.</span></span> <span data-ttu-id="25966-116">Por último, el código ajusta el valor de nuevo para el intervalo de cero a 255 original y copia los datos en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="25966-116">Finally, the code adjusts the value again for the original zero-to-255 range and copies the data to the output buffer.</span></span> <span data-ttu-id="25966-117">En el código de ejemplo siguiente se procesa el vídeo UYVY.</span><span class="sxs-lookup"><span data-stu-id="25966-117">The following example code processes UYVY video.</span></span> <span data-ttu-id="25966-118">En este formato, cada otro byte es un valor U o Y.</span><span class="sxs-lookup"><span data-stu-id="25966-118">In this format, every other byte is a U or Y value.</span></span>


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



<span data-ttu-id="25966-119">En el vídeo RGB, la información de color y luminancia se codifica como valores de rojo, verde y azul distintos.</span><span class="sxs-lookup"><span data-stu-id="25966-119">For RGB video, the color and luminance information is encoded as separate red, green, and blue values.</span></span> <span data-ttu-id="25966-120">El complemento de ejemplo calcula el promedio de los tres valores para determinar el valor de Gray y, a continuación, ajusta cada valor de color mediante el factor de escala proporcionado.</span><span class="sxs-lookup"><span data-stu-id="25966-120">The sample plug-in computes the average of the three values to determine the value for gray, and then adjusts each color value by using the supplied scale factor.</span></span> <span data-ttu-id="25966-121">Una vez más, los valores se deben normalizar para el intervalo de-128 a 127 antes de la escala.</span><span class="sxs-lookup"><span data-stu-id="25966-121">Once again, the values must be normalized for the -128 to 127 range before scaling.</span></span> <span data-ttu-id="25966-122">El siguiente código de Process32Bit muestra el proceso de RGB32:</span><span class="sxs-lookup"><span data-stu-id="25966-122">The following code from Process32Bit shows the process for RGB32:</span></span>


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



<span data-ttu-id="25966-123">Para obtener más información acerca de los formatos de vídeo, consulte el [sitio web de FourCC](../directshow/fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="25966-123">For more information about video formats, see the [FourCC website](../directshow/fourcc-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="25966-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="25966-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25966-125">**Implementación de un complemento DSP de vídeo**</span><span class="sxs-lookup"><span data-stu-id="25966-125">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 