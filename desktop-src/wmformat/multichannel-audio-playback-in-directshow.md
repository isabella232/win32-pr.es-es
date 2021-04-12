---
title: Reproducción de audio multicanal en DirectShow
description: Reproducción de audio multicanal en DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows Media Format SDK, DirectShow
- SDK de Windows Media Format, reproducción de audio multicanal
- SDK de Windows Media Format, reproducción de audio
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), reproducción de audio multicanal
- ASF (formato de sistemas avanzados), reproducción de audio multicanal
- Advanced Systems Format (ASF), reproducción de audio
- ASF (formato de sistemas avanzados), reproducción de audio
- DirectShow, reproducción de audio multicanal
- DirectShow, reproducción de audio
- audio multicanal, reproducción
- reproducción de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c6eec473c8bbbff81d35f4127d5d132d0b6cd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420339"
---
# <a name="multichannel-audio-playback-in-directshow"></a>Reproducción de audio multicanal en DirectShow

Para reproducir un archivo Windows Media Audio multicanal en DirectShow, debe establecer la \_ propiedad "HIRESOUTPUT" directamente en el descodificador después de haberse conectado al lector ASF de WM. No es necesario configurar el objeto de lector. Sin embargo, para trabajar con DMO directamente, necesita wmcodecconst. h del código de [ejemplo para usar el](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en) paquete de descarga de interfaces de códec de vídeo y Windows Media Audio.

**Nota:** Este procedimiento de configuración solo se admite para los archivos que no están protegidos por Rights Management digital.

Los pasos básicos para habilitar la salida multicanal son los siguientes:

1.  Llame a RenderFile para crear el gráfico de filtro.
2.  Obtener un puntero al filtro de contenedor de DMO
3.  Desconectar el contenedor DMO del representador de audio
4.  Establezca la \_ propiedad "HIRESOUTPUT" en el descodificador.
5.  Vuelva a conectar el contenedor DMO y el representador de audio.
6.  Ejecute el gráfico.

En los fragmentos de código siguientes se muestran estos pasos. (Todas las comprobaciones de errores se han omitido por razones de simplicidad. Debe agregar rutinas de control de errores adecuadas si usa este código en una aplicación).


```C++
    ...
    //ENABLE MULTICHANNEL OUTPUT
    //Render the file
    hr = m_pGraphBuilder->RenderFile(wFileName, NULL);

    // Get pointers to the two DMO Wrapper interfaces we need.
    // (Function bodies provided at the end of this snippet.)
    hr = GetDMOWrapper(pGB, &m_pDMOBaseFilter, &m_pWrapper); 

    //Disconnect the DMO Wrapper from the Audio Renderer
    CComPtr<IPin> pDMOOut;
    CComPtr<IPin> pRendererIn;
    hr = GetPin(m_pDMOBaseFilter, PINDIR_OUTPUT, &pDMOOut);
    hr = pDMOOut->ConnectedTo(&pRendererIn);
    hr = pDMOOut->Disconnect();
    hr = pRendererIn->Disconnect();

    //Set the property on the DMO
    VARIANT varg;
    ::VariantInit(&varg);
    varg.vt    = VT_BOOL;
    varg.boolVal = TRUE;
    CComQIPtr<IMediaObject, &IID_IMediaObject> pMediaObject(m_pWrapper);
    CComQIPtr<IPropertyBag, &IID_IPropertyBag> pPropertyBag(pMediaObject);
    hr = pPropertyBag->Write(g_wszWMACHiResOutput, &varg);

    // Reconnect the DMO Wrapper and the Audio Renderer
    hr = pGB->Connect(pDMOOut, pRendererIn);
    //END MULTICHANNEL (now the graph can be run)
...

```



Las funciones GetDMOWrapper y GetPin del fragmento de código anterior se implementan de la siguiente manera:


```C++
// In this example, the IBaseFilter and IDMOWrapperFilter interfaces are
// declared  at global scope
HRESULT GetDMOWrapper (IFilterGraph *pGraph, IBaseFilter** m_pDMOBaseFilter, IDMOWrapperFilter** m_pWrapper) 
{
    CComPtr<IEnumFilters> pEnum;
    CComPtr<IBaseFilter> pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        // If we find the IDMOWrapperFilter interface, that means we 
        // have the DMO Wrapper filter. Store both interfaces for future use.
        CComPtr<IDMOWrapperFilter> pWrapper;
        hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, (void**) &pWrapper);
        if (SUCCEEDED(hr))
        {
            *m_pWrapper = pWrapper.Detach();
            *m_pDMOBaseFilter = pFilter.Detach();
            return S_OK;
        }

        pFilter.Release();
    }

    return E_FAIL;
}

HRESULT GetPin(IBaseFilter *pFilter, PIN_DIRECTION PinDir, IPin** ppPin)
{
    CComPtr<IEnumPins>  pEnum;
    CComPtr<IPin>       pPin;

         HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        return hr;
    }
    while(pEnum->Next(1, &pPin, 0) == S_OK)
    {
        PIN_DIRECTION PinDirThis;
        pPin->QueryDirection(&PinDirThis);
        if (PinDir == PinDirThis)
        {
            *ppPin = pPin.Detach();
            return S_OK;
        }
        pPin.Release();
    }
    
    return E_FAIL;
}
```



 

 




