---
description: Cómo obtener eventos del origen de red
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: Cómo obtener eventos del origen de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474269"
---
# <a name="how-to-get-events-from-the-network-source"></a>Cómo obtener eventos del origen de red

La resolución de origen permite a una aplicación crear un origen de red y abrir una conexión a una dirección URL específica. El origen de red genera eventos para marcar el principio y el final de la operación asincrónica de apertura de una conexión. Una aplicación puede registrarse para estos eventos mediante la [**interfaz IMFSourceOpenMonitor.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)

Esta interfaz expone el método [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) al que el origen de red llama directamente cuando abre la dirección URL de forma asincrónica. El origen de red notifica a la aplicación cuando comienza a abrir la dirección URL generando el [evento MEConnectStart.](meconnectstart.md) A continuación, el origen de red [genera el evento MEConnectEnd](meconnectend.md) cuando completa la operación de apertura.

> [!Note]  
> Para enviar estos eventos a la aplicación, el origen de red no usa la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) porque estos eventos se generan antes de que se cree el origen de red. La aplicación puede obtener todos los demás eventos de origen de red mediante la interfaz **DEGMEDIAEventGenerator** de la sesión multimedia.

 

## <a name="to-get-events-from-the-network-source"></a>Para obtener eventos del origen de red

1.  Implemente [**la interfaz IMFSourceOpenMonitor.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) En la implementación del [**método IMFSourceOpenMonitor::OnSourceEvent,**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) haga lo siguiente:
    1.  Para obtener el estado del evento, llame [**a IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus). Este método indica si la operación que desencadenó el evento, como una llamada al método de resolución de origen, se ha hecho correctamente. Si la operación no se realiza correctamente, el estado es un código de error.
    2.  Procese el evento en función del tipo de evento: [MEConnectStart](meconnectstart.md) o [MEConnectEnd](meconnectend.md), que la aplicación puede obtener llamando a [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).
2.  Configure un par clave-valor en un objeto de almacén de propiedades para almacenar un puntero a la implementación [**DEFUSOURCEOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) descrita en el paso 1.
    1.  Cree un objeto de almacén de propiedades llamando a la **función PSCreateMemoryPropertyStore.**
    2.  Establezca la [**propiedad MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) en una **estructura PROPERTYKEY.**
    3.  Proporcione el valor de datos de tipo UNKNOWN de VT en una estructura PROPVARIANT estableciendo el puntero IUnknown en la implementación de la aplicación de la interfaz \_ [**IMFSourceOpenMonitor.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)  
    4.  Establezca el par clave-valor en el almacén de propiedades mediante una llamada **a IPropertyStore::SetValue**.
3.  Pase el puntero del almacén de propiedades a los métodos de resolución de origen que usa la aplicación para crear el origen de red, como [**POR ejemplo, IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) y otros.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo implementar la interfaz [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) para obtener eventos del origen de red.


```C++
class CSourceOpenMonitor : public IMFSourceOpenMonitor
{
public:
    CSourceOpenMonitor () : m_cRef(1) { }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CSourceOpenMonitor, IMFSourceOpenMonitor),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        // For thread safety, return a temporary variable.
        return cRef;
    }


    STDMETHODIMP OnSourceEvent(IMFMediaEvent* pEvent)
    {
        MediaEventType eventType = MEUnknown;   // Event type
        HRESULT hrStatus = S_OK;                // Event status

        // Get the event type.
        HRESULT hr = pEvent->GetType(&eventType);

        // Get the event status. If the operation that triggered the event
        // did not succeed, the status is a failure code.
        if (SUCCEEDED(hr))
        {
            hr = pEvent->GetStatus(&hrStatus);
        }

        if (FAILED(hrStatus))
        {
            hr = hrStatus;
        }

        if (SUCCEEDED(hr))
        {
            // Switch on the event type.
            switch(eventType)
            {
                case MEConnectStart:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connecting...\n");
                    break;

                case MEConnectEnd:
                    // The application does something. (Not shown.)
                    OutputDebugString(L"Connect End.\n");
                    break;
            }
        }
        else
        {
            // Event failed.
            // The application handled a failure. (Not shown.)
        }
        return S_OK;
    }
private:
    long    m_cRef;
};
```



En el ejemplo siguiente se muestra cómo establecer la [**propiedad MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) en el origen de red al abrir la dirección URL:


```C++
HRESULT CreateMediaSourceWithSourceOpenMonitor(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    CSourceOpenMonitor *pMonitor = new (std::nothrow) CSourceOpenMonitor();

    if (pMonitor == NULL)
    {
        return E_OUTOFMEMORY;
    }

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        var.vt = VT_UNKNOWN;
        pMonitor->QueryInterface(IID_PPV_ARGS(&var.punkVal));

        hr = pConfig->SetValue(MFPKEY_SourceOpenMonitor, var);

        PropVariantClear(&var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    SafeRelease(&pMonitor);

    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Redes en Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



