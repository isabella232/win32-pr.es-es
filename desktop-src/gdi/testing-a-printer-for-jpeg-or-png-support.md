---
description: La función SetDIBitsToDevice usa datos de color de una DIB para establecer los píxeles del rectángulo especificado en el dispositivo asociado al contexto del dispositivo de destino.
ms.assetid: 7cbb2b7a-2d95-4352-9e75-aa814e8f01bd
title: Probar una impresora para obtener compatibilidad con JPEG o PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8a83671c8ca0e64395e58c2275f343413e9563996ff4372e19d2512bfc5b7e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885737"
---
# <a name="testing-a-printer-for-jpeg-or-png-support"></a>Probar una impresora para obtener compatibilidad con JPEG o PNG

La [**función SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) usa datos de color de una DIB para establecer los píxeles del rectángulo especificado en el dispositivo asociado al contexto del dispositivo de destino.

[**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) se extiende para permitir que una imagen JPEG o PNG se pase como la imagen de origen.

Por ejemplo:


```C++
// 
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
               pvJpgImage, nJpgImageSize, sizeof(ul), &ul) > 0) &&

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
    // Do the SetDIBitsToDevice. 
    // 

    iRet = SetDIBitsToDevice(hdc,
                             ulDstX, ulDstY,
                             ulDstWidth, ulDstHeight,
                             0, 0,
                             0, ulJpgHeight,
                             pvJpgImage,
                             &bmi,
                             DIB_RGB_COLORS);

    if (iRet == GDI_ERROR)
        return FALSE;
}
else
{
    // 
    // Decompress image into a DIB and call SetDIBitsToDevice  
    // with the DIB instead. 
    // 
}
```



 

 



