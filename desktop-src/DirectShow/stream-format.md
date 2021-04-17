---
description: Formato de secuencia
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Formato de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688211"
---
# <a name="stream-format"></a>Formato de secuencia

Tanto el controlador MSDV como el controlador UVC pueden generar dos formatos DV: vídeo de audio entrelazado o vídeo. Audio entrelazado: vídeo es el formato original del dispositivo. El formato de solo vídeo contiene los mismos datos, pero los ejemplos se marcan como sin datos de audio. El formato de solo vídeo existe principalmente para la compatibilidad con aplicaciones que usan vídeo para Windows. Para obtener más información, consulte [archivos AVI de tipo 1 frente a tipo-2](type-1-vs--type-2-dv-avi-files.md).

**Controlador MSDV**

El controlador MSDV tiene dos clavijas de salida. El primer PIN de salida envía datos intercalados y el segundo solo envía datos de vídeo. Solo se puede conectar un PIN de salida a la vez. Para seleccionar un formato, conecte el PIN de salida adecuado. Puede usar la interfaz [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) en el PIN de salida para buscar el formato.

**Controlador UVC**

A diferencia del controlador MSDV, el controlador UVC proporciona ambos formatos del mismo pin. El formato predeterminado es solo vídeo. Para seleccionar el formato, use la interfaz **IAMStreamConfig** en el terminal de salida. Llame al método **GetStreamCaps** para enumerar los tipos de medios en el terminal de salida. Para cada tipo de medio, si el tipo principal coincide con el formato deseado, llame a **SetFormat** y pase dicho tipo de medio.



| Formato                      | Tipo principal             |
|-----------------------------|------------------------|
| Audio y vídeo intercalados | MEDIATYPE \_ intercalado |
| Solo vídeo                  | Vídeo de MEDIATYPE \_       |



 

La función siguiente establece el formato basado en el GUID de tipo principal.


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



El controlador MSDV también admite **IAMStreamConfig**, por lo que puede escribir código que funcione para ambos tipos de dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocámara DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



