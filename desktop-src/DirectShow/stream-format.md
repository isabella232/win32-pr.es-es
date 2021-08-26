---
description: Formato de secuencia
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Formato de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01ed1ac4501a2d8f081c12fef75baf15aaebd442fc182a116db1038c2a73523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903995"
---
# <a name="stream-format"></a>Formato de secuencia

Tanto el controlador MSDV como el controlador UVC pueden generar dos formatos DV: audio-vídeo intercalado o solo vídeo. El audio y vídeo intercalado es el formato original del dispositivo. El formato de solo vídeo contiene los mismos datos, pero los ejemplos se marcan como que no tienen datos de audio. El formato de solo vídeo existe principalmente por compatibilidad con aplicaciones que usan Video para Windows. Para obtener más información, [vea Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).

**Controlador MSDV**

El controlador MSDV tiene dos pines de salida. El primer pin de salida envía datos intercalados y el segundo envía datos de solo vídeo. Solo se puede conectar un pin de salida a la vez. Para seleccionar un formato, conecte el pin de salida adecuado. Puede usar la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) en el pin de salida para buscar el formato.

**Controlador UVC**

A diferencia del controlador MSDV, el controlador UVC ofrece ambos formatos desde el mismo pin. El formato predeterminado es de solo vídeo. Para seleccionar el formato, use la **interfaz IAMStreamConfig** en el pin de salida. Llame al **método GetStreamCaps** para enumerar los tipos de medios en el pin de salida. Para cada tipo de medio, si el tipo principal coincide con el formato deseado, llame a **SetFormat** y pase ese tipo de medio.



| Formato                      | Tipo principal             |
|-----------------------------|------------------------|
| Audio y vídeo intercalados | MEDIATYPE \_ intercalado |
| Solo vídeo                  | Vídeo \_ MEDIATYPE       |



 

La función siguiente establece el formato en función del GUID de tipo principal.


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



El controlador MSDV también admite **IAMStreamConfig,** por lo que puede escribir código que funcione para ambos tipos de dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una cámara dv](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



