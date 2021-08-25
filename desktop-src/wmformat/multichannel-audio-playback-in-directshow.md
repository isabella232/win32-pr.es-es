---
title: Reproducción de audio multicanal en DirectShow
description: Reproducción de audio multicanal en DirectShow
ms.assetid: 5123854a-0f1f-40f4-bf57-47622b91103f
keywords:
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia, reproducción de audio multicanal
- Windows SDK de formato multimedia, reproducción de audio
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Formato de sistemas avanzados (ASF), reproducción de audio multicanal
- ASF (formato de sistemas avanzados), reproducción de audio multicanal
- Formato de sistemas avanzados (ASF), reproducción de audio
- ASF (formato de sistemas avanzados), reproducción de audio
- DirectShow de audio multicanal
- DirectShow,reproducción de audio
- audio multicanal, reproducción
- reproducción de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99734ddf32be6e0340e26fafef0f22f1127ec3652cc0db0a9d2e94ce2f694b96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808165"
---
# <a name="multichannel-audio-playback-in-directshow"></a>Reproducción de audio multicanal en DirectShow

Para reproducir un archivo de audio multimedia Windows multicanal en DirectShow, debe establecer la propiedad "HIRESOUTPUT" directamente en el descodificador después de que se haya conectado al lector \_ DE ASF wm. No es necesaria ninguna configuración del objeto reader. Sin embargo, para trabajar directamente con DMO, necesita wmcodecconst.h del código de ejemplo para usar el paquete de descarga Windows [Media Audio and Video Codec Interfaces.](https://www.microsoft.com/downloads/details.aspx?FamilyId=92490D8A-4F2E-46F1-8835-B1D987B3C985&displaylang=en)

**Nota** Este procedimiento de configuración solo se admite para los archivos que no están protegidos por Digital Rights Management.

Los pasos básicos para habilitar la salida multicanal son los siguientes:

1.  Llame a RenderFile para crear el gráfico de filtro.
2.  Obtener un puntero al filtro DMO contenedor
3.  Desconectar el contenedor DMO del representador de audio
4.  Establezca la \_ propiedad "HIRESOUTPUT" en el descodificador.
5.  Vuelva a conectar DMO contenedor y el representador de audio.
6.  Ejecute el gráfico.

Los fragmentos de código siguientes muestran estos pasos. (Se ha omitido toda la comprobación de errores por motivos de simplicidad. Debe agregar rutinas de control de errores adecuadas si usa este código en una aplicación).


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



 

 




