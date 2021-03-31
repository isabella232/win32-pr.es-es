---
description: Paso 3 implementación de la función Frame-Grabbing
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: Paso 3 implementación de la función Frame-Grabbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97f585ff365e40ec611a9e11ce365839aa87be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911706"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a>Paso 3: implementar la función Frame-Grabbing

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Este tema es el paso 3 de [capturar un fotograma de póster](grabbing-a-poster-frame.md).

El siguiente paso consiste en implementar la función GetBitmap, que usa el detector de medios para capturar un fotograma de póster. Dentro de esta función, realice los pasos siguientes:

1.  Cree el detector de medios.
2.  Especifique un archivo multimedia.
3.  Examine cada secuencia del archivo. Si se trata de un flujo de vídeo, obtenga las dimensiones nativas del vídeo.
4.  Obtener un fotograma de póster, especificando el tiempo de búsqueda y la dimensión de destino.

Cree el objeto de detector de medios llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



Especifique un nombre de archivo mediante el método [**IMediaDet::p el \_ nombre**](imediadet-put-filename.md) de archivo. Este método toma un parámetro **BSTR** .


```C++
hr = pDet->put_Filename(bstrFilename);
```



Obtiene el número de secuencias y recorre en bucle cada flujo que comprueba el tipo de medio. El método [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) recupera el número de secuencias y el método [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) especifica la secuencia que se va a examinar. Salga del bucle en la primera secuencia de vídeo.


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



Si no se encuentra ningún flujo de vídeo, la función se cierra.

En el código anterior, el método [**IMediaDet:: get \_ StreamType**](imediadet-get-streamtype.md) devuelve solo el GUID de tipo principal. Esto resulta práctico si no necesita examinar el tipo de medio completo. Sin embargo, para obtener las dimensiones de vídeo, es necesario examinar el bloque de formato, por lo que se necesita el tipo de medio completo. Puede recuperarlo llamando al método [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md) , que rellena una estructura de [**\_ \_ tipo media AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) . El detector de medios convierte todos los flujos de vídeo en formato sin comprimir, con un bloque de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



El método [**Get \_ StreamMediaType**](imediadet-get-streammediatype.md) asigna el bloque de formato, que el llamador debe liberar. En este ejemplo se usa la función [**FreeMediaType**](freemediatype.md) de la biblioteca de clases base.

Ahora está listo para obtener el fotograma del póster. En primer lugar, llame al método [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) con un puntero **nulo** para el búfer:


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



Esta llamada devuelve el tamaño de búfer necesario en el parámetro *Lsize* . El primer parámetro especifica el tiempo de flujo en el que se va a buscar; en este ejemplo se usa la hora cero. Para el ancho y el alto, en este ejemplo se usan las dimensiones de vídeo nativas obtenidas anteriormente. Si especifica otros valores, el detector de medios extenderá el mapa de bits para que coincida.

Si el método se ejecuta correctamente, asigne el búfer y llame de nuevo a [**GetBitmapBits**](imediadet-getbitmapbits.md) :


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



Esta es la función completa, con un control de errores algo mejor.


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



Siguiente: [paso 4: dibujo del mapa de bits en el área cliente](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captación de un fotograma de póster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
