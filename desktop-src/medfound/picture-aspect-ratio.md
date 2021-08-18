---
description: 'En este tema se describen dos conceptos relacionados: la relación de aspecto de imagen y la relación de aspecto de píxeles.'
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Relación de aspecto de la imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae59cf213a9d44c9075f33be4bd422b81ced6dea270cf4fc9408990442529e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972987"
---
# <a name="picture-aspect-ratio"></a>Relación de aspecto de la imagen

En este tema se describen dos conceptos relacionados: la relación de aspecto de imagen y la relación de aspecto de píxeles. A continuación, describe cómo se expresan estos conceptos Microsoft Media Foundation tipos de medios.

-   [Relación de aspecto de la imagen](#picture-aspect-ratio)
    -   [Letterboxing](#letterboxing)
    -   [Panorámica y examen](#pan-and-scan)
-   [Proporción de aspecto de píxeles](#pixel-aspect-ratio)
-   [Trabajar con relaciones de aspecto](#working-with-aspect-ratios)
-   [Ejemplos de código](#code-examples)
    -   [Buscar el área de presentación](#finding-the-display-area)
    -   [Conversión entre las relaciones de aspecto de píxeles](#converting-between-pixel-aspect-ratios)
    -   [Calcular el área de cuadro de letras](#calculating-the-letterbox-area)
-   [Temas relacionados](#related-topics)

## <a name="picture-aspect-ratio"></a>Relación de aspecto de la imagen

*La relación de aspecto* de la imagen define la forma de la imagen de vídeo mostrada. La relación de aspecto de la imagen se nota X:Y, donde X:Y es la relación entre el ancho de imagen y el alto de la imagen. La mayoría de los estándares de vídeo usan una relación de aspecto de imagen de 4:3 o 16:9. La relación de aspecto 16:9 se denomina normalmente *widescreen.* A menudo usa una relación de aspecto de 1:85:1 o 1:66:1. La relación de aspecto de imagen también se denomina *relación de aspecto de pantalla* (DAR).

![diagrama que muestra las relaciones de aspecto 4:3 y 16:9](images/aspect-ratio01.png)

A veces, la imagen de vídeo no tiene la misma forma que el área de presentación. Por ejemplo, un vídeo 4:3 podría mostrarse en un televisor de pantalla ancha (16×9). En el vídeo del equipo, el vídeo puede mostrarse dentro de una ventana que tiene un tamaño arbitrario. En ese caso, hay tres maneras de hacer que la imagen quepa dentro del área de presentación:

-   Ajuste la imagen a lo largo de un eje para ajustarla al área de presentación.
-   Escale la imagen para ajustarla al área de visualización, manteniendo al mismo tiempo la relación de aspecto de la imagen original.
-   Recorte la imagen.

El ajuste de la imagen para ajustarse al área de presentación es casi siempre incorrecto, ya que no conserva la relación de aspecto de la imagen correcta.

### <a name="letterboxing"></a>Letterboxing

El proceso de escalado de una imagen de pantalla ancha para ajustarse a una pantalla de 4:3 se denomina *letterboxing*, que se muestra en el diagrama siguiente. Las áreas rectanglulares resultantes en la parte superior e inferior de la imagen normalmente se rellenan con negro, aunque se pueden usar otros colores.

![diagrama en el que se muestra la manera correcta de usar letterbox](images/aspect-ratio02.png)

El caso inverso, el escalado de una imagen de 4:3 para ajustarse a una pantalla ancha, a veces se denomina *pillarboxing*. Sin embargo, el término *cuadro de letras* también se usa en un sentido general, para significar el escalado de una imagen de vídeo para ajustarse a cualquier área de visualización determinada.

![diagrama en el que se muestra pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>Panorámica y examen

El análisis panorámico es una técnica por la que una imagen de pantalla ancha se recorta a un área rectangular de 4×3, para mostrarse en un dispositivo de pantalla de 4:3. La imagen resultante rellena toda la pantalla, sin necesidad de áreas de cuadro de letras negras, pero las partes de la imagen original se recortan fuera de la imagen. El área recortada puede moverse de marco a marco, a medida que cambia el área de interés. El término "panorámica" en *desplazamiento* panorámico y examen hace referencia al efecto de desplazamiento panorámico que se produce al mover el área de desplazamiento panorámico y examen.

![diagrama en el que se muestra la panorámica y el examen](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>Proporción de aspecto de píxeles

*La relación de aspecto* de píxeles (PAR) mide la forma de un píxel.

Cuando se captura una imagen digital, la imagen se muestrea vertical y horizontalmente, lo que da lugar a una matriz rectangular de muestras cuantificadas, *denominadas píxeles* *o pór.* La forma de la cuadrícula de muestreo determina la forma de los píxeles de la imagen digitalizado.

Este es un ejemplo que usa números pequeños para mantener la matemática simple. Supongamos que la imagen original es cuadrada (es decir, la relación de aspecto de la imagen es 1:1); y supongamos que la cuadrícula de muestreo contiene 12 elementos, organizados en una cuadrícula de 4×3. La forma de cada píxel resultante será más alta que la ancha. En concreto, la forma de cada píxel será 3×4. Los píxeles que no son cuadrados se *denominan píxeles no cuadrados.*

![diagrama que muestra una cuadrícula de muestreo no cuadrada](images/aspect-ratio05.png)

La relación de aspecto de píxeles también se aplica al dispositivo de pantalla. La forma física del dispositivo de pantalla y la resolución de píxeles física (a través y hacia abajo) determinan el PAR del dispositivo de pantalla. Los monitores de equipo suelen usar píxeles cuadrados. Si la imagen PAR y la pantalla PAR no coinciden, la imagen se debe escalar en una dimensión, ya sea vertical u horizontalmente, para que se muestre correctamente. La fórmula siguiente relaciona PAR, la relación de aspecto de pantalla (DAR) y el tamaño de la imagen en píxeles:

*DAR* = ( ancho *de imagen en píxeles*  /  *alto de imagen en píxeles*) × *PAR*

Tenga en cuenta que el ancho de imagen y el alto de la imagen en esta fórmula hacen referencia a la imagen en memoria, no a la imagen mostrada.

Este es un ejemplo real: el vídeo análogo NEE-M contiene 480 líneas de examen en el área de imagen activa. ITU-R Rec. BT.601 especifica una velocidad de muestreo horizontal de 704 píxeles visibles por línea, lo que produce una imagen digital con 704 x 480 píxeles. La relación de aspecto de la imagen prevista es 4:3, lo que produce un PAR de 10:11.

-   DAR: 4:3
-   Ancho en píxeles: 704
-   Alto en píxeles: 480
-   PAR: 11/10/10

4/3 = (704/420) x (10/11)

Para mostrar esta imagen correctamente en un dispositivo de visualización con píxeles cuadrados, debe escalar el ancho en 10/11 o el alto en 11/10.

## <a name="working-with-aspect-ratios"></a>Trabajar con relaciones de aspecto

La forma correcta de un fotograma de vídeo se define mediante la relación de aspecto *de píxeles* (PAR) y el *área de visualización*.

-   El PAR define la forma de los píxeles de una imagen. Los píxeles cuadrados tienen una relación de aspecto de 1:1. Cualquier otra relación de aspecto describe un píxel no cuadrado. Por ejemplo, la televisión UNOS usa un PAR de 10:11. Suponiendo que va a presentar el vídeo en un monitor de equipo, la pantalla tendrá píxeles cuadrados (1:1 PAR). El PAR del contenido de origen se da en el atributo [**MF MT PIXEL ASPECT \_ \_ \_ \_ RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) en el tipo de medio.
-   El área de presentación es la región de la imagen de vídeo que se va a mostrar. Hay dos áreas de visualización pertinentes que se pueden especificar en el tipo de medio:
    -   Apertura de panorámica y examen. La apertura de panorámica y examen es una región de 4×3 de vídeo que debe mostrarse en modo de panorámica y examen. Se usa para mostrar contenido de pantalla ancha en una pantalla de 4×3 sin cuadro de texto. La apertura de panorámica y examen se da en el atributo [**MF MT PAN SCAN \_ \_ \_ \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md) y solo se debe usar cuando el atributo [**MF MT PAN SCAN \_ \_ \_ \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md) es **TRUE.**
    -   Apertura de la pantalla. Esta apertura se define en algunos estándares de vídeo. Cualquier cosa fuera de la apertura de la pantalla es la región de sobresalido y no debe mostrarse. Por ejemplo, el televisor PX es de 720× 480 píxeles con una apertura de pantalla de 704×480. La apertura de la pantalla se da en el atributo [**MF MT MINIMUM DISPLAY \_ \_ \_ \_ APERTURE.**](mf-mt-minimum-display-aperture-attribute.md) Si está presente, se debe usar cuando el modo de panorámica y examen es **FALSE.**

Si el modo de panorámica y can es **FALSE** y no se define ninguna apertura de pantalla, se debe mostrar todo el fotograma de vídeo. De hecho, este es el caso de la mayoría del contenido de vídeo que no sea televisión y vídeo de DVD. La relación de aspecto de toda la imagen se calcula como *(* alto del área de presentación del ancho del área de presentación ) ×  /   *PAR*.

## <a name="code-examples"></a>Ejemplos de código

### <a name="finding-the-display-area"></a>Buscar el área de presentación

El código siguiente muestra cómo obtener el área de presentación del tipo de medio.


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



### <a name="converting-between-pixel-aspect-ratios"></a>Conversión entre las relaciones de aspecto de píxeles

En el código siguiente se muestra cómo convertir un rectángulo de una relación de aspecto de píxeles (PAR) a otra, a la vez que se conserva la relación de aspecto de la imagen.


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



### <a name="calculating-the-letterbox-area"></a>Calcular el área de cuadro de letras

El código siguiente calcula el área de cuadro de letras, dado un rectángulo de origen y destino. Se supone que ambos rectángulos tienen el mismo PAR.


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

[**APERTURA \_ DE PANTALLA MÍNIMA \_ DE \_ \_ MF MT**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**RELACIÓN \_ DE ASPECTO DE \_ \_ PÍXELES MF MT \_**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



