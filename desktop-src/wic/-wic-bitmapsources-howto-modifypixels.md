---
description: En este tema se muestra cómo modificar los píxeles de un origen de mapa de bits mediante los componentes IWICBitmap y IWICBitmapLock.
ms.assetid: a08af015-bc42-4a31-af03-106714b08d08
title: Cómo modificar los píxeles de un origen de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8be623d540fcd313476ea5c7ec5e724231d33aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706498"
---
# <a name="how-to-modify-the-pixels-of-a-bitmap-source"></a>Cómo modificar los píxeles de un origen de mapa de bits

En este tema se muestra cómo modificar los píxeles de un origen de mapa de bits mediante los componentes [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) y [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .

Para modificar los píxeles de un origen de mapa de bits

1.  Cree un objeto [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) para crear objetos de Windows Imaging Component (WIC).

    ```C++
    // Create WIC factory
    hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pIWICFactory)
        );
    ```

    

2.  Use el método [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) para crear un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) a partir de un archivo de imagen.

    ```C++
    HRESULT hr = S_OK;

    IWICBitmapDecoder *pIDecoder = NULL;
    IWICBitmapFrameDecode *pIDecoderFrame  = NULL;

    hr = m_pIWICFactory->CreateDecoderFromFilename(
       L"turtle.jpg",                  // Image to be decoded
       NULL,                           // Do not prefer a particular vendor
       GENERIC_READ,                   // Desired read access to the file
       WICDecodeMetadataCacheOnDemand, // Cache metadata when needed
       &pIDecoder                      // Pointer to the decoder
       );
    ```

    

3.  Obtiene el primer [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) de la imagen.

    ```C++
    // Retrieve the first bitmap frame.
    if (SUCCEEDED(hr))
    {
       hr = pIDecoder->GetFrame(0, &pIDecoderFrame);
    }
    ```

    

    El formato de archivo JPEG solo admite un único fotograma. Dado que el archivo de este ejemplo es un archivo JPEG, se usa el primer fotograma ( `0` ). Para obtener información sobre los formatos de imagen que tienen varios fotogramas, consulte [recuperación de los marcos de una imagen](-wic-bitmapsources-howto-retrieveimageframes.md) para tener acceso a cada fotograma de la imagen.

4.  Cree un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) a partir del fotograma de imagen obtenido previamente.

    ```C++
    IWICBitmap *pIBitmap = NULL;
    IWICBitmapLock *pILock = NULL;

    UINT uiWidth = 10;
    UINT uiHeight = 10;

    WICRect rcLock = { 0, 0, uiWidth, uiHeight };

    // Create the bitmap from the image frame.
    if (SUCCEEDED(hr))
    {
       hr = m_pIWICFactory->CreateBitmapFromSource(
          pIDecoderFrame,          // Create a bitmap from the image frame
          WICBitmapCacheOnDemand,  // Cache metadata when needed
          &pIBitmap);              // Pointer to the bitmap
    }
    ```

    

5.  Obtiene un [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) para un rectángulo especificado de [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap).

    ```C++
    if (SUCCEEDED(hr))
    {
       // Obtain a bitmap lock for exclusive write.
       // The lock is for a 10x10 rectangle starting at the top left of the
       // bitmap.
       hr = pIBitmap->Lock(&rcLock, WICBitmapLockWrite, &pILock);
    ```

    

6.  Procesa los datos de píxeles que ahora están bloqueados por el objeto [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .

    ```C++
       if (SUCCEEDED(hr))
       {
          UINT cbBufferSize = 0;
          BYTE *pv = NULL;

          // Retrieve a pointer to the pixel data.
          if (SUCCEEDED(hr))
          {
             hr = pILock->GetDataPointer(&cbBufferSize, &pv);
          }
          
          // Pixel manipulation using the image data pointer pv.
          // ...

          // Release the bitmap lock.
          SafeRelease(&pILock);
       }
    }
    ```

    

    Para desbloquear [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), llame a [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en todos los objetos [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) asociados al **IWICBitmap**.

7.  Limpie los objetos creados.

    ```C++
    SafeRelease(&pIBitmap);
    SafeRelease(&pIDecoder);
    SafeRelease(&pIDecoderFrame);
    ```

    

## <a name="see-also"></a>Consulte también

[Guía de programación](-wic-programming-guide.md)


[Referencia](-wic-codec-reference.md)


[Muestras](-wic-samples.md)


 

 
