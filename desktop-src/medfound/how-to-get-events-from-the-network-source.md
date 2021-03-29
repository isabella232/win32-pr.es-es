---
description: Cómo obtener eventos desde el origen de red
ms.assetid: 46869f52-323c-41ec-95f7-e7e5d177b782
title: Cómo obtener eventos desde el origen de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100241b069ae8976c20c68b6055571d5ff1e5c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811336"
---
# <a name="how-to-get-events-from-the-network-source"></a><span data-ttu-id="a3a9c-103">Cómo obtener eventos desde el origen de red</span><span class="sxs-lookup"><span data-stu-id="a3a9c-103">How to Get Events from the Network Source</span></span>

<span data-ttu-id="a3a9c-104">La resolución de origen permite a una aplicación crear un origen de red y abrir una conexión a una dirección URL específica.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-104">The source resolver enables an application to create a network source and open a connection to a specific URL.</span></span> <span data-ttu-id="a3a9c-105">El origen de red genera eventos para marcar el principio y el final de la operación asincrónica de abrir una conexión.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-105">The network source raises events to mark the beginning and the end of the asynchronous operation of opening a connection.</span></span> <span data-ttu-id="a3a9c-106">Una aplicación se puede registrar para estos eventos mediante la interfaz [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="a3a9c-106">An application can register for these events by using the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>

<span data-ttu-id="a3a9c-107">Esta interfaz expone el método [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) al que el origen de red llama directamente cuando abre la dirección URL de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-107">This interface exposes the [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method that the network source calls directly when it opens the URL asynchronously.</span></span> <span data-ttu-id="a3a9c-108">El origen de red notifica a la aplicación cuando comienza a abrir la dirección URL generando el evento [MEConnectStart](meconnectstart.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a9c-108">The network source notifies the application when it starts opening the URL by raising the [MEConnectStart](meconnectstart.md) event.</span></span> <span data-ttu-id="a3a9c-109">Después, el origen de red genera el evento [MEConnectEnd](meconnectend.md) cuando finaliza la operación de apertura.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-109">The network source then raises the [MEConnectEnd](meconnectend.md) event when it completes the open operation.</span></span>

> [!Note]  
> <span data-ttu-id="a3a9c-110">Para enviar estos eventos a la aplicación, el origen de red no utiliza la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) porque estos eventos se generan antes de que se cree el origen de red.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-110">To send these events to the application, the network source does not use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface because these events are raised before the network source is created.</span></span> <span data-ttu-id="a3a9c-111">La aplicación puede obtener todos los demás eventos de origen de red mediante la interfaz **IMFMediaEventGenerator** de la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-111">The application can get all other network source events by using the Media Session's **IMFMediaEventGenerator** interface.</span></span>

 

## <a name="to-get-events-from-the-network-source"></a><span data-ttu-id="a3a9c-112">Para obtener eventos del origen de red</span><span class="sxs-lookup"><span data-stu-id="a3a9c-112">To get events from the network source</span></span>

1.  <span data-ttu-id="a3a9c-113">Implemente la interfaz [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="a3a9c-113">Implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span> <span data-ttu-id="a3a9c-114">En la implementación del método [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a3a9c-114">In your implementation of [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, do the following:</span></span>
    1.  <span data-ttu-id="a3a9c-115">Obtiene el estado del evento llamando a [**IMFMediaEvent:: getStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span><span class="sxs-lookup"><span data-stu-id="a3a9c-115">Get the event status by calling [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus).</span></span> <span data-ttu-id="a3a9c-116">Este método indica si la operación que desencadenó el evento, como una llamada al método de resolución de origen, se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-116">This method indicates whether the operation that triggered the event, such as a source resolver method call, succeeded.</span></span> <span data-ttu-id="a3a9c-117">Si la operación no se realiza correctamente, el estado es un código de error.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-117">If the operation is not successful, the status is a failure code.</span></span>
    2.  <span data-ttu-id="a3a9c-118">Procese el evento en función del tipo de evento: [MEConnectStart](meconnectstart.md) o [MEConnectEnd](meconnectend.md), que la aplicación puede obtener llamando a [**IMFMediaEvent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span><span class="sxs-lookup"><span data-stu-id="a3a9c-118">Process the event based on the event type: [MEConnectStart](meconnectstart.md) or [MEConnectEnd](meconnectend.md), which the application can get by calling [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype).</span></span>
2.  <span data-ttu-id="a3a9c-119">Configure un par clave-valor en un objeto de almacén de propiedades para almacenar un puntero a la implementación de [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) que se describe en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-119">Configure a key-value pair in a property store object to store a pointer to the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) implementation described in step 1.</span></span>
    1.  <span data-ttu-id="a3a9c-120">Cree un objeto de almacén de propiedades mediante una llamada a la función **PSCreateMemoryPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="a3a9c-120">Create a property store object by calling the **PSCreateMemoryPropertyStore** function.</span></span>
    2.  <span data-ttu-id="a3a9c-121">Establezca la propiedad [**MFPKEY \_ SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) en una estructura **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="a3a9c-121">Set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property in a **PROPERTYKEY** structure.</span></span>
    3.  <span data-ttu-id="a3a9c-122">Proporcione el \_ valor de datos de tipo desconocido VT en una estructura **PROPVARIANT** estableciendo el puntero **IUnknown** en la implementación de la aplicación de la interfaz [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) .</span><span class="sxs-lookup"><span data-stu-id="a3a9c-122">Provide the VT\_UNKNOWN type data value in a **PROPVARIANT** structure by setting the **IUnknown** pointer to the application's implementation of the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>
    4.  <span data-ttu-id="a3a9c-123">Establezca el par clave-valor en el almacén de propiedades mediante una llamada a **IPropertyStore:: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-123">Set the key-value pair in the property store by calling **IPropertyStore::SetValue**.</span></span>
3.  <span data-ttu-id="a3a9c-124">Pase el puntero del almacén de propiedades a los métodos de resolución de origen que usa la aplicación para crear el origen de red, como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) y otros.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-124">Pass the property store pointer to the source resolver methods that the application is using to create the network source, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) and others.</span></span>

## <a name="example"></a><span data-ttu-id="a3a9c-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3a9c-125">Example</span></span>

<span data-ttu-id="a3a9c-126">En el ejemplo siguiente se muestra cómo implementar la interfaz [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) para obtener los eventos del origen de red.</span><span class="sxs-lookup"><span data-stu-id="a3a9c-126">The following example shows how to implement the [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface to get events from the network source.</span></span>


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



<span data-ttu-id="a3a9c-127">En el ejemplo siguiente se muestra cómo establecer la propiedad [**\_ SourceOpenMonitor de MFPKEY**](mfpkey-sourceopenmonitor-property.md) en el origen de red al abrir la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="a3a9c-127">The following example shows how to set the [**MFPKEY\_SourceOpenMonitor**](mfpkey-sourceopenmonitor-property.md) property on the network source when you open the URL:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a3a9c-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3a9c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3a9c-129">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a3a9c-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



