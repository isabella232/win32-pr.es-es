---
title: Para enumerar los formatos de entrada
description: Para enumerar los formatos de entrada
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Formato de sistemas avanzados (ASF), enumeración de formatos de entrada
- ASF (formato de sistemas avanzados), enumeración de formatos de entrada
- perfiles, enumeración de formatos de entrada
- códecs, enumeración de formatos de entrada
- Formato de sistemas avanzados (ASF), enumeraciones de formato de entrada
- ASF (formato de sistemas avanzados), enumeraciones de formato de entrada
- profiles,enumeraciones de formato de entrada
- codecs,enumeraciones de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09e1583c9331e9cfab26e7ac64064224111ea58858d32b876ece843b83df0d2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929255"
---
# <a name="to-enumerate-input-formats"></a>Para enumerar los formatos de entrada

Cada uno de los códecs Windows media acepta uno o varios tipos de medios de entrada para la compresión. El SDK Windows Media Format le permite introducir una variedad más amplia de formatos que los admitidos por los códecs. Para ello, el SDK realiza transformaciones de procesamiento previo en las entradas cuando es necesario, como el cambio de tamaño de fotogramas de vídeo o el cambio de tamaño del audio. En cualquier caso, debe asegurarse de que los formatos de entrada de los archivos que escribe coinciden con los datos que envía al escritor. Cada códec tiene un formato de medio de entrada predeterminado que se establece en el escritor cuando se carga el perfil. Puede examinar el formato de entrada predeterminado llamando a [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).

Los códecs de vídeo admiten los siguientes formatos: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 y RGB 8. Los códecs de audio admiten audio PCM.

Para enumerar los formatos de entrada admitidos por un códec, realice los pasos siguientes:

1.  Cree un objeto de escritor y establezca un perfil que se usará. Para obtener más información sobre cómo establecer perfiles en el sistema de escritura, vea [Para usar perfiles con el escritor](to-use-profiles-with-the-writer.md).
2.  Identifique el número de entrada para el que desea comprobar los formatos. Para obtener más información sobre cómo identificar números de entrada, vea [Para identificar entradas por número.](to-identify-inputs-by-number.md)
3.  Recupere el número total de formatos de entrada admitidos por la entrada deseada llamando a [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).
4.  Recorre en bucle todos los formatos de entrada admitidos y realiza los pasos siguientes para cada uno.
    -   Recupere la [**interfaz IWMInputMediaProps para el**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) formato de entrada llamando a [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).
    -   Recupere la [**estructura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para el formato de entrada. Llame [**a IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)y pase **NULL** para que el *parámetro pType* obtenga el tamaño de la estructura. A continuación, asigne memoria para contener la estructura y llame **de nuevo a GetMediaType** para obtener la estructura. [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) hereda de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), por lo que puede realizar las llamadas a **GetMediaType** desde la instancia de **IWMInputMediaProps** recuperada en el paso anterior.
    -   El formato descrito en la [**estructura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contiene toda la información pertinente sobre el formato de entrada. El formato básico del medio se identifica mediante **WM \_ MEDIA \_ TYPE.subtype**. En el caso de las secuencias de vídeo, el miembro **pbFormat** apunta a una estructura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) asignada dinámicamente que contiene más detalles sobre la secuencia, incluido el tamaño del rectángulo. No es necesario que el tamaño de los fotogramas de entrada coincida exactamente con un tamaño admitido por el códec. Si no coinciden, los componentes en tiempo de ejecución del SDK, en muchos casos, cambiarán automáticamente el tamaño de los fotogramas de vídeo de entrada a algo que el códec pueda aceptar.

El código de ejemplo siguiente busca el formato de entrada del subtipo pasado como parámetro. Para obtener más información sobre el uso de este código, vea [Usar los ejemplos de código](using-the-code-examples.md).


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMWriter (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Escritura de archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




