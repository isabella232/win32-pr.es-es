---
title: Para enumerar los formatos de entrada
description: Para enumerar los formatos de entrada
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Advanced Systems Format (ASF), enumerar formatos de entrada
- ASF (formato de sistemas avanzados), enumerar formatos de entrada
- perfiles, enumerar formatos de entrada
- códecs, enumerar formatos de entrada
- Advanced Systems Format (ASF), enumeraciones de formato de entrada
- ASF (formato de sistemas avanzados), enumeraciones de formato de entrada
- perfiles, enumeraciones de formato de entrada
- códecs, enumeraciones de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077447"
---
# <a name="to-enumerate-input-formats"></a>Para enumerar los formatos de entrada

Cada uno de los códecs de Windows Media acepta uno o más tipos de medios de entrada para la compresión. El SDK de Windows Media Format permite especificar una mayor variedad de formatos que los que admiten los códecs. Para ello, el SDK realiza transformaciones previas al procesamiento en las entradas cuando es necesario, como cambiar el tamaño de los fotogramas de vídeo o volver a muestrear el audio. En cualquier caso, debe asegurarse de que los formatos de entrada de los archivos que escribe coinciden con los datos que envía al escritor. Cada códec tiene un formato de medio de entrada predeterminado que se establece en el escritor cuando se carga el perfil. Puede examinar el formato de entrada predeterminado llamando a [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).

Los códecs de vídeo admiten los formatos siguientes: IYUV, i420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 y RGB 8. Los códecs de audio admiten audio PCM.

Para enumerar los formatos de entrada admitidos por un códec, realice los pasos siguientes:

1.  Cree un objeto de escritor y establezca un perfil para usarlo. Para obtener más información sobre la configuración de perfiles en el escritor, vea [para usar perfiles con el escritor](to-use-profiles-with-the-writer.md).
2.  Identifique el número de entrada para el que desea comprobar los formatos. Para obtener más información acerca de la identificación de números de entrada, consulte [para identificar entradas por número](to-identify-inputs-by-number.md).
3.  Recupere el número total de formatos de entrada admitidos por la entrada deseada llamando a [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).
4.  Recorra en bucle todos los formatos de entrada admitidos y realice los pasos siguientes para cada uno.
    -   Recupere la interfaz [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para el formato de entrada mediante una llamada a [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).
    -   Recupere la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para el formato de entrada. Llame a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), pasando **null** para el parámetro *pType* para obtener el tamaño de la estructura. A continuación, asigne memoria para que contenga la estructura y llame de nuevo a **GetMediaType** para obtener la estructura. [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) hereda de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), por lo que puede realizar las llamadas a **GetMediaType** desde la instancia de **IWMInputMediaProps** recuperada en el paso anterior.
    -   El formato descrito en la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contiene toda la información pertinente sobre el formato de entrada. El formato básico de los medios se identifica mediante el **tipo de medio de WM \_ \_ . SubType**. En el caso de las secuencias de vídeo, el miembro **pbFormat** apunta a una estructura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) asignada dinámicamente que contiene más detalles sobre la secuencia, incluido el tamaño del rectángulo. No es necesario que el tamaño de los fotogramas de entrada coincida exactamente con el que admite el códec. Si no coinciden, los componentes en tiempo de ejecución del SDK, en muchos casos, cambiarán automáticamente el tamaño de los fotogramas de vídeo de entrada a algo que pueda aceptar el códec.

En el código de ejemplo siguiente se busca el formato de entrada del subtipo que se pasa como parámetro. Para obtener más información sobre el uso de este código, vea [usar los ejemplos de código](using-the-code-examples.md).


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

[**Interfaz IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Escribir archivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




