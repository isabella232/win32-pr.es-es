---
description: La función StretchDIBits copia los datos de color de un rectángulo de píxeles de un DIB al rectángulo de destino especificado.
ms.assetid: d4e3f631-3852-4cee-8e97-2244c39b200e
title: Ajustar el tamaño de una imagen JPEG o PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cd5bf3cbef8bab80d45536d90bfdd10174c26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985382"
---
# <a name="sizing-a-jpeg-or-png-image"></a><span data-ttu-id="e806b-103">Ajustar el tamaño de una imagen JPEG o PNG</span><span class="sxs-lookup"><span data-stu-id="e806b-103">Sizing a JPEG or PNG Image</span></span>

<span data-ttu-id="e806b-104">La función [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) copia los datos de color de un rectángulo de píxeles de un DIB al rectángulo de destino especificado.</span><span class="sxs-lookup"><span data-stu-id="e806b-104">The [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) function copies the color data for a rectangle of pixels in a DIB to the specified destination rectangle.</span></span> <span data-ttu-id="e806b-105">Si el rectángulo de destino es mayor que el rectángulo de origen, esta función estira las filas y columnas de los datos de color para ajustarse al rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="e806b-105">If the destination rectangle is larger than the source rectangle, this function stretches the rows and columns of color data to fit the destination rectangle.</span></span> <span data-ttu-id="e806b-106">Si el rectángulo de destino es menor que el rectángulo de origen, **StretchDIBits** comprime las filas y las columnas usando la operación de trama especificada.</span><span class="sxs-lookup"><span data-stu-id="e806b-106">If the destination rectangle is smaller than the source rectangle, **StretchDIBits** compresses the rows and columns by using the specified raster operation.</span></span>

<span data-ttu-id="e806b-107">[**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) se extiende para permitir que se pase una imagen JPEG o PNG como imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="e806b-107">[**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) is extended to allow a JPEG or PNG image to be passed as the source image.</span></span>

<span data-ttu-id="e806b-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e806b-108">For example:</span></span>


```C++
// pvJpgImage points to a buffer containing the JPEG image 
// nJpgImageSize is the size of the buffer 
// ulJpgWidth is the width of the JPEG image 
// ulJpgHeight is the height of the JPEG image 
// 

// 
// Check if CHECKJPEGFORMAT is supported (device has JPEG support) 
// and use it to verify that device can handle the JPEG image. 
// 

ul = CHECKJPEGFORMAT;

if (
    // Check if CHECKJPEGFORMAT exists: 

    (ExtEscape(hdc, QUERYESCSUPPORT,
               sizeof(ul), &ul, 0, 0) > 0) &&

    // Check if CHECKJPEGFORMAT executed without error: 

    (ExtEscape(hdc, CHECKJPEGFORMAT,
               nJpgImageSize, pvJpgImage, sizeof(ul), &ul) > 0) &&

    // Check status code returned by CHECKJPEGFORMAT: 

    (ul == 1)
   )
{
    // 
    // Initialize the BITMAPINFO. 
    // 

    memset(&bmi, 0, sizeof(bmi));
    bmi.bmiHeader.biSize        = sizeof(BITMAPINFOHEADER);
    bmi.bmiHeader.biWidth       = ulJpgWidth;
    bmi.bmiHeader.biHeight      = -ulJpgHeight; // top-down image 
    bmi.bmiHeader.biPlanes      = 1;
    bmi.bmiHeader.biBitCount    = 0;
    bmi.bmiHeader.biCompression = BI_JPEG;
    bmi.bmiHeader.biSizeImage   = nJpgImageSize;

    // 
    // Do the StretchDIBits. 
    // 

    iRet = StretchDIBits(hdc,
                         // destination rectangle 
                         ulDstX, ulDstY, ulDstWidth, ulDstHeight,
                         // source rectangle 
                         0, 0, ulJpgWidth, ulJpgHeight,
                         pvJpgImage,
                         &bmi,
                         DIB_RGB_COLORS,
                         SRCCOPY);

    if (iRet == GDI_ERROR)
        return FALSE;
}
else
{
    // 
    // Decompress image into a DIB and call StretchDIBits  
    // with the DIB instead. 
    // 
}
```



 

 



