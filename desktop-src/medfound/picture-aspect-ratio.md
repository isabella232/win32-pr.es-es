---
description: En este tema se describen dos conceptos relacionados, la relación de aspecto de la imagen y la relación de aspecto de píxeles.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Relación de aspecto de la imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275826"
---
# <a name="picture-aspect-ratio"></a>Relación de aspecto de la imagen

En este tema se describen dos conceptos relacionados, la relación de aspecto de la imagen y la relación de aspecto de píxeles. A continuación, describe cómo se expresan estos conceptos en Microsoft Media Foundation mediante tipos de medios.

-   [Relación de aspecto de la imagen](#picture-aspect-ratio)
    -   [Formato letterbox](#letterboxing)
    -   [Pan y SCAN](#pan-and-scan)
-   [Relación de aspecto de píxeles](#pixel-aspect-ratio)
-   [Trabajar con relaciones de aspecto](#working-with-aspect-ratios)
-   [Ejemplos de código](#code-examples)
    -   [Buscar el área de presentación](#finding-the-display-area)
    -   [Conversión entre proporciones de aspecto de píxeles](#converting-between-pixel-aspect-ratios)
    -   [Calcular el área de panorámica](#calculating-the-letterbox-area)
-   [Temas relacionados](#related-topics)

## <a name="picture-aspect-ratio"></a>Relación de aspecto de la imagen

La *relación de aspecto* de la imagen define la forma de la imagen de vídeo mostrada. La relación de aspecto de la imagen es X:Y, donde X:Y es la relación del ancho de la imagen con el alto de la imagen. La mayoría de los estándares de vídeo usan una relación de aspecto de imagen 4:3 o 16:9. La relación de aspecto 16:9 se denomina normalmente *pantalla panorámica*. Película de cine suele usar una relación de aspecto 1:85:1 o 1:66:1. La relación de aspecto de la imagen también se denomina *Mostrar relación de aspecto* (dar).

![diagrama que muestra las relaciones de aspecto 4:3 y 16:9](images/aspect-ratio01.png)

A veces, la imagen de vídeo no tiene la misma forma que el área de visualización. Por ejemplo, un vídeo 4:3 podría aparecer en un televisor de pantalla panorámica (16 × 9). En el vídeo del equipo, es posible que el vídeo se muestre en una ventana que tenga un tamaño arbitrario. En ese caso, hay tres maneras de crear la imagen para que quepa en el área de presentación:

-   Estire la imagen a lo largo de un eje para ajustarla al área de visualización.
-   Escale la imagen para que quepa en el área de visualización, manteniendo la relación de aspecto de la imagen original.
-   Recortar la imagen.

La ampliación de la imagen para que quepa en el área de presentación casi siempre es incorrecta, ya que no conserva la relación de aspecto de la imagen correcta.

### <a name="letterboxing"></a>Formato letterbox

El proceso de escalado de una imagen de pantalla panorámica para ajustarse a una pantalla 4:3 se denomina *panorámica*, que se muestra en el diagrama siguiente. Las áreas de rectanglular resultantes de la parte superior e inferior de la imagen se rellenan normalmente con negro, aunque se pueden usar otros colores.

![diagrama que muestra la manera correcta de la panorámica](images/aspect-ratio02.png)

El caso inverso, el escalado de una imagen 4:3 para ajustarse a una pantalla panorámica, a veces se denomina *pillarboxing*. Sin embargo, el término *panorámica* también se usa en sentido general, para hacer que el escalado de una imagen de vídeo se ajuste a cualquier área de presentación determinada.

![diagrama que muestra pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>Pan y SCAN

Pan-and-Scan es una técnica por la que una imagen de pantalla panorámica se recorta a una zona rectangular de 4 × 3, para su presentación en un dispositivo de pantalla 4:3. La imagen resultante llena toda la presentación, sin necesidad de áreas de pantalla ancha negra, pero las partes de la imagen original se recortan de la imagen. El área que se recorta puede moverse de un marco a un marco, a medida que el área de interés se desplaza. El término "pan" en *pan-and-Scan* hace referencia al efecto de movimiento panorámico que se produce al mover el área de desplazamiento y exploración.

![diagrama que muestra la panorámica y el recorrido](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>Relación de aspecto de píxeles

*Relación de aspecto de píxeles* (par) mide la forma de un píxel.

Cuando se captura una imagen digital, la imagen se muestrea tanto vertical como horizontalmente, lo que da como resultado una matriz rectangular de muestras cuantificadas, denominada *píxeles* o *Pels*. La forma de la cuadrícula de muestreo determina la forma de los píxeles de la imagen digitalizada.

A continuación se muestra un ejemplo en el que se usan pequeños números para simplificar la matemática. Supongamos que la imagen original es cuadrada (es decir, la relación de aspecto de la imagen es 1:1); y Supongamos que la cuadrícula de muestreo contiene 12 elementos, organizados en una cuadrícula de 4 × 3. La forma de cada píxel resultante será más alta de lo ancho. En concreto, la forma de cada píxel será 3 × 4. Los píxeles que no son cuadrados se denominan *píxeles no cuadrados*.

![diagrama que muestra una cuadrícula de muestreo no cuadrada](images/aspect-ratio05.png)

La relación de aspecto de píxeles también se aplica al dispositivo de pantalla. La forma física del dispositivo de pantalla y la resolución de píxeles físicos (en horizontal y vertical) determinan el PAR del dispositivo de pantalla. Los monitores de equipo suelen usar píxeles cuadrados. Si el PAR de la imagen y el PAR de la pantalla no coinciden, la imagen se debe escalar en una dimensión, ya sea vertical u horizontalmente, para que se muestre correctamente. La siguiente fórmula relaciona el PAR, la relación de aspecto de la pantalla (DAR) y el tamaño de la imagen en píxeles:

*Dar* = (*ancho de la imagen en píxeles*  /  *alto en píxeles*) × *par*

Tenga en cuenta que el ancho de la imagen y el alto de la imagen en esta fórmula hacen referencia a la imagen en memoria, no a la imagen mostrada.

Este es un ejemplo del mundo real: el vídeo analógico NTSC-M contiene 480 líneas de análisis en el área de la imagen activa. ITU-R Rec. BT. 601 especifica una velocidad de muestreo horizontal de 704 píxeles visibles por línea, lo que produce una imagen digital con 704 x 480 píxeles. La relación de aspecto de la imagen deseada es 4:3, lo que da como resultado un PAR de 10:11.

-   DAR: 4:3
-   Ancho en píxeles: 704
-   Alto en píxeles: 480
-   PAR: 10/11

4/3 = (704/420) x (10/11)

Para que la imagen se muestre correctamente en un dispositivo de pantalla con píxeles cuadrados, debe escalar el ancho entre el 10/11 y el alto 11/10.

## <a name="working-with-aspect-ratios"></a>Trabajar con relaciones de aspecto

La forma correcta de un fotograma de vídeo se define mediante la *relación de aspecto de píxeles* (par) y el área de *visualización*.

-   El PAR define la forma de los píxeles de una imagen. Los píxeles cuadrados tienen una relación de aspecto de 1:1. Cualquier otra relación de aspecto describe un píxel no cuadrado. Por ejemplo, NTSC Television usa un PAR de 10:11. Suponiendo que está presentando el vídeo en un monitor de equipo, la pantalla tendrá píxeles cuadrados (1:1 PAR). El PAR de contenido de origen se proporciona en el atributo de [**\_ \_ \_ \_ relación de aspecto MF MT**](mf-mt-pixel-aspect-ratio-attribute.md) en el tipo de medio.
-   El área de visualización es la región de la imagen de vídeo que se va a mostrar. Hay dos áreas de presentación relevantes que pueden especificarse en el tipo de medio:
    -   Abertura de pan y SCAN. La abertura de pan-and-Scan es una región de vídeo de 4 × 3 que se debe mostrar en el modo Pan/Scan. Se usa para mostrar el contenido de pantalla ancha en una pantalla de 4 x 3 sin el uso de la panorámica. La abertura de pan-and-Scan se proporciona en el atributo [**MF \_ MT \_ pan \_ scan \_ abertura**](mf-mt-pan-scan-aperture-attribute.md) y debe usarse solo cuando el atributo [**MF \_ MT \_ pan \_ scan \_ habilitado**](mf-mt-pan-scan-enabled-attribute.md) es **true**.
    -   Mostrar abertura. Esta abertura se define en algunos estándares de vídeo. Todo lo que esté fuera de la abertura de pantalla es la región de sobrebarrido y no debe mostrarse. Por ejemplo, la televisión NTSC tiene 720 × 480 píxeles con una abertura de pantalla de 704 × 480. La abertura de pantalla se proporciona en el atributo [**MF \_ MT \_ Minimum \_ Display \_ abertura**](mf-mt-minimum-display-aperture-attribute.md) . Si está presente, se debe usar cuando el modo de desplazamiento y exploración es **falso**.

Si el modo de pan y Can es **false** y no se ha definido ninguna abertura de pantalla, se debe mostrar todo el fotograma de vídeo. De hecho, este es el caso de la mayoría del contenido de vídeo que no sea el vídeo de televisión y DVD. La relación de aspecto de la imagen completa se calcula como *(alto del área de* presentación de la  /  *pantalla*) × *par*.

## <a name="code-examples"></a>Ejemplos de código

### <a name="finding-the-display-area"></a>Buscar el área de presentación

En el código siguiente se muestra cómo obtener el área de visualización del tipo de medio.


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a>Conversión entre proporciones de aspecto de píxeles

En el código siguiente se muestra cómo convertir un rectángulo de una relación de aspecto de píxel (PAR) a otra, a la vez que se conserva la relación de aspecto de la imagen.


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a>Calcular el área de panorámica

En el código siguiente se calcula el área de panorámica, dados un rectángulo de origen y de destino. Se supone que ambos rectángulos tienen el mismo PAR.


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de medios](media-types.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[**\_ \_ apertura mínima de \_ pantalla MF MT \_**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_apertura de \_ \_ análisis panorámico MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**examen de pan de MF \_ MT \_ \_ \_ habilitado**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**\_relación de \_ aspecto de píxeles MF MT \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



