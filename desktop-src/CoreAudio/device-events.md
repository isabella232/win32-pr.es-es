---
description: Eventos de dispositivo
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Eventos de dispositivo (API de audio Core)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0513fc49ee5f3cb2bfe95ca2330cb79b74720923
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659313"
---
# <a name="device-events-core-audio-apis"></a><span data-ttu-id="641ff-103">Eventos de dispositivo (API de audio Core)</span><span class="sxs-lookup"><span data-stu-id="641ff-103">Device Events (Core Audio APIs)</span></span>

<span data-ttu-id="641ff-104">Un evento de dispositivo notifica a los clientes de un cambio en el estado de un [dispositivo de punto de conexión de audio](audio-endpoint-devices.md) en el sistema.</span><span class="sxs-lookup"><span data-stu-id="641ff-104">A device event notifies clients of a change in the status of an [audio endpoint device](audio-endpoint-devices.md) in the system.</span></span> <span data-ttu-id="641ff-105">A continuación se muestran ejemplos de eventos de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="641ff-105">The following are examples of device events:</span></span>

-   <span data-ttu-id="641ff-106">El usuario habilita o deshabilita un dispositivo de extremo de audio desde Administrador de dispositivos o desde el panel de control multimedia de Windows, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="641ff-106">The user enables or disables an audio endpoint device from Device Manager or from the Windows multimedia control panel, Mmsys.cpl.</span></span>
-   <span data-ttu-id="641ff-107">El usuario agrega un adaptador de audio al sistema o quita un adaptador de audio del sistema.</span><span class="sxs-lookup"><span data-stu-id="641ff-107">The user adds an audio adapter to the system or removes an audio adapter from the system.</span></span>
-   <span data-ttu-id="641ff-108">El usuario conecta un dispositivo de punto de conexión de audio a un conector de audio con la detección de la presencia de conector o quita un dispositivo de punto de conexión de audio de este conector.</span><span class="sxs-lookup"><span data-stu-id="641ff-108">The user plugs an audio endpoint device into an audio jack with jack-presence detection, or removes an audio endpoint device from such a jack.</span></span>
-   <span data-ttu-id="641ff-109">El usuario cambia el [rol de dispositivo](device-roles.md) que se asigna a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-109">The user changes the [device role](device-roles.md) that is assigned to a device.</span></span>
-   <span data-ttu-id="641ff-110">El valor de una [propiedad de un dispositivo](device-properties.md) cambia.</span><span class="sxs-lookup"><span data-stu-id="641ff-110">The value of a [property of a device](device-properties.md) changes.</span></span>

<span data-ttu-id="641ff-111">La adición o eliminación de un adaptador de audio genera eventos de dispositivo para todos los dispositivos de punto de conexión de audio que se conectan al adaptador.</span><span class="sxs-lookup"><span data-stu-id="641ff-111">The addition or removal of an audio adapter generates device events for all of the audio endpoint devices that connect to the adapter.</span></span> <span data-ttu-id="641ff-112">Los primeros cuatro elementos de la lista anterior son ejemplos de cambios de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-112">The first four items in the preceding list are examples of device state changes.</span></span> <span data-ttu-id="641ff-113">Para obtener más información sobre los Estados de dispositivo de los dispositivos de punto de conexión de audio, consulte [constantes de estado de dispositivo \_ \_ XXX](device-state-xxx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="641ff-113">For more information about the device states of audio endpoint devices, see [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).</span></span> <span data-ttu-id="641ff-114">Para obtener más información sobre la detección de la presencia de tomas, consulte [dispositivos de punto de conexión de audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="641ff-114">For more information about jack-presence detection, see [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="641ff-115">Un cliente puede registrarse para recibir notificaciones cuando se producen eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-115">A client can register to be notified when device events occur.</span></span> <span data-ttu-id="641ff-116">En respuesta a estas notificaciones, el cliente puede cambiar dinámicamente la manera en que usa un dispositivo determinado o seleccionar un dispositivo diferente para usarlo con un fin determinado.</span><span class="sxs-lookup"><span data-stu-id="641ff-116">In response to these notifications, the client can dynamically change the way that it uses a particular device, or select a different device to use for a particular purpose.</span></span>

<span data-ttu-id="641ff-117">Por ejemplo, si una aplicación está reproduciendo una pista de audio a través de un conjunto de altavoces USB y el usuario desconecta los altavoces del conector USB, la aplicación recibe una notificación de evento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-117">For example, if an application is playing an audio track through a set of USB speakers, and the user disconnects the speakers from the USB connector, the application receives a device-event notification.</span></span> <span data-ttu-id="641ff-118">En respuesta al evento, si la aplicación detecta que un conjunto de oradores del escritorio está conectado al adaptador de audio integrado en la placa base del sistema, la aplicación puede reanudar la reproducción de la pista de audio a través de los altavoces del escritorio.</span><span class="sxs-lookup"><span data-stu-id="641ff-118">In response to the event, if the application detects that a set of desktop speakers is connected to the integrated audio adapter on the system motherboard, the application can resume playing the audio track through the desktop speakers.</span></span> <span data-ttu-id="641ff-119">En este ejemplo, la transición de los altavoces USB a los altavoces de escritorio se produce automáticamente, sin necesidad de que el usuario intervenga mediante la redirección explícita de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="641ff-119">In this example, the transition from USB speakers to desktop speakers occurs automatically, without requiring the user to intervene by explicitly redirecting the application.</span></span>

<span data-ttu-id="641ff-120">Para registrarse para recibir notificaciones de dispositivo, un cliente llama al método [**IMMDeviceEnumerator:: RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="641ff-120">To register to receive device notifications, a client calls the [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) method.</span></span> <span data-ttu-id="641ff-121">Cuando el cliente ya no requiere notificaciones, los cancela llamando al método [**IMMDeviceEnumerator:: UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) .</span><span class="sxs-lookup"><span data-stu-id="641ff-121">When the client no longer requires notifications, it cancels them by calling the [**IMMDeviceEnumerator::UnregisterEndpointNotificationCallback**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) method.</span></span> <span data-ttu-id="641ff-122">Ambos métodos toman un parámetro de entrada, denominado *pNotify*, que es un puntero a una instancia de la interfaz [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) .</span><span class="sxs-lookup"><span data-stu-id="641ff-122">Both methods take an input parameter, named *pNotify*, that is a pointer to an [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) interface instance.</span></span>

<span data-ttu-id="641ff-123">Un cliente implementa la interfaz **IMMNotificationClient** .</span><span class="sxs-lookup"><span data-stu-id="641ff-123">The **IMMNotificationClient** interface is implemented by a client.</span></span> <span data-ttu-id="641ff-124">La interfaz contiene varios métodos, cada uno de los cuales actúa como una rutina de devolución de llamada para un tipo determinado de evento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-124">The interface contains several methods, each of which serves as a callback routine for a particular type of device event.</span></span> <span data-ttu-id="641ff-125">Cuando se produce un evento de dispositivo en un dispositivo de punto de conexión de audio, el módulo MMDevice llama al método adecuado en la interfaz **IMMNotificationClient** de cada cliente que está registrado actualmente para recibir notificaciones de eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-125">When a device event occurs in an audio endpoint device, the MMDevice module calls the appropriate method in the **IMMNotificationClient** interface of every client that is currently registered to receive device-event notifications.</span></span> <span data-ttu-id="641ff-126">Estas llamadas pasan una descripción del evento a los clientes.</span><span class="sxs-lookup"><span data-stu-id="641ff-126">These calls pass a description of the event to the clients.</span></span> <span data-ttu-id="641ff-127">Para obtener más información, vea [**IMMNotificationClient (interfaz**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)).</span><span class="sxs-lookup"><span data-stu-id="641ff-127">For more information, see [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span>

<span data-ttu-id="641ff-128">Un cliente que está registrado para recibir notificaciones de eventos de dispositivo recibirá notificaciones de todos los tipos de eventos de dispositivo que se producen en todos los dispositivos de punto de conexión de audio del sistema.</span><span class="sxs-lookup"><span data-stu-id="641ff-128">A client that is registered to receive device-event notifications will receive notifications of all types of device events that occur in all of the audio endpoint devices in the system.</span></span> <span data-ttu-id="641ff-129">Si un cliente solo está interesado en determinados tipos de eventos o en determinados dispositivos, los métodos de su implementación de **IMMNotificationClient** deben filtrar los eventos de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="641ff-129">If a client is interested only in certain event types or in certain devices, then the methods in its **IMMNotificationClient** implementation should filter the events appropriately.</span></span>

<span data-ttu-id="641ff-130">El Windows SDK proporciona ejemplos que incluyen varias implementaciones para la [**interfaz IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span><span class="sxs-lookup"><span data-stu-id="641ff-130">The Windows SDK provides samples that include several implementations for the [**IMMNotificationClient Interface**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient).</span></span> <span data-ttu-id="641ff-131">Para obtener más información, consulte [ejemplos de SDK que usan las API de audio principales](sdk-samples-that-use-the-core-audio-apis.md).</span><span class="sxs-lookup"><span data-stu-id="641ff-131">For more information, see [SDK Samples That Use the Core Audio APIs](sdk-samples-that-use-the-core-audio-apis.md).</span></span>

<span data-ttu-id="641ff-132">En el ejemplo de código siguiente se muestra una posible implementación de la interfaz **IMMNotificationClient** :</span><span class="sxs-lookup"><span data-stu-id="641ff-132">The following code example shows a possible implementation of the **IMMNotificationClient** interface:</span></span>


```C++
//-----------------------------------------------------------
// Example implementation of IMMNotificationClient interface.
// When the status of audio endpoint devices change, the
// MMDevice module calls these methods to notify the client.
//-----------------------------------------------------------

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class CMMNotificationClient : public IMMNotificationClient
{
    LONG _cRef;
    IMMDeviceEnumerator *_pEnumerator;

    // Private function to print device-friendly name
    HRESULT _PrintDeviceName(LPCWSTR  pwstrId);

public:
    CMMNotificationClient() :
        _cRef(1),
        _pEnumerator(NULL)
    {
    }

    ~CMMNotificationClient()
    {
        SAFE_RELEASE(_pEnumerator)
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IMMNotificationClient) == riid)
        {
            AddRef();
            *ppvInterface = (IMMNotificationClient*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback methods for device-event notifications.

    HRESULT STDMETHODCALLTYPE OnDefaultDeviceChanged(
                                EDataFlow flow, ERole role,
                                LPCWSTR pwstrDeviceId)
    {
        char  *pszFlow = "?????";
        char  *pszRole = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (flow)
        {
        case eRender:
            pszFlow = "eRender";
            break;
        case eCapture:
            pszFlow = "eCapture";
            break;
        }

        switch (role)
        {
        case eConsole:
            pszRole = "eConsole";
            break;
        case eMultimedia:
            pszRole = "eMultimedia";
            break;
        case eCommunications:
            pszRole = "eCommunications";
            break;
        }

        printf("  -->New default device: flow = %s, role = %s\n",
               pszFlow, pszRole);
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceAdded(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Added device\n");
        return S_OK;
    };

    HRESULT STDMETHODCALLTYPE OnDeviceRemoved(LPCWSTR pwstrDeviceId)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Removed device\n");
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnDeviceStateChanged(
                                LPCWSTR pwstrDeviceId,
                                DWORD dwNewState)
    {
        char  *pszState = "?????";

        _PrintDeviceName(pwstrDeviceId);

        switch (dwNewState)
        {
        case DEVICE_STATE_ACTIVE:
            pszState = "ACTIVE";
            break;
        case DEVICE_STATE_DISABLED:
            pszState = "DISABLED";
            break;
        case DEVICE_STATE_NOTPRESENT:
            pszState = "NOTPRESENT";
            break;
        case DEVICE_STATE_UNPLUGGED:
            pszState = "UNPLUGGED";
            break;
        }

        printf("  -->New device state is DEVICE_STATE_%s (0x%8.8x)\n",
               pszState, dwNewState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnPropertyValueChanged(
                                LPCWSTR pwstrDeviceId,
                                const PROPERTYKEY key)
    {
        _PrintDeviceName(pwstrDeviceId);

        printf("  -->Changed device property "
               "{%8.8x-%4.4x-%4.4x-%2.2x%2.2x-%2.2x%2.2x%2.2x%2.2x%2.2x%2.2x}#%d\n",
               key.fmtid.Data1, key.fmtid.Data2, key.fmtid.Data3,
               key.fmtid.Data4[0], key.fmtid.Data4[1],
               key.fmtid.Data4[2], key.fmtid.Data4[3],
               key.fmtid.Data4[4], key.fmtid.Data4[5],
               key.fmtid.Data4[6], key.fmtid.Data4[7],
               key.pid);
        return S_OK;
    }
};

// Given an endpoint ID string, print the friendly device name.
HRESULT CMMNotificationClient::_PrintDeviceName(LPCWSTR pwstrId)
{
    HRESULT hr = S_OK;
    IMMDevice *pDevice = NULL;
    IPropertyStore *pProps = NULL;
    PROPVARIANT varString;

    CoInitialize(NULL);
    PropVariantInit(&varString);

    if (_pEnumerator == NULL)
    {
        // Get enumerator for audio endpoint devices.
        hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                              NULL, CLSCTX_INPROC_SERVER,
                              __uuidof(IMMDeviceEnumerator),
                              (void**)&_pEnumerator);
    }
    if (hr == S_OK)
    {
        hr = _pEnumerator->GetDevice(pwstrId, &pDevice);
    }
    if (hr == S_OK)
    {
        hr = pDevice->OpenPropertyStore(STGM_READ, &pProps);
    }
    if (hr == S_OK)
    {
        // Get the endpoint device's friendly-name property.
        hr = pProps->GetValue(PKEY_Device_FriendlyName, &varString);
    }
    printf("----------------------\nDevice name: \"%S\"\n"
           "  Endpoint ID string: \"%S\"\n",
           (hr == S_OK) ? varString.pwszVal : L"null device",
           (pwstrId != NULL) ? pwstrId : L"null ID");

    PropVariantClear(&varString);

    SAFE_RELEASE(pProps)
    SAFE_RELEASE(pDevice)
    CoUninitialize();
    return hr;
}
```



<span data-ttu-id="641ff-133">La clase CMMNotificationClient del ejemplo de código anterior es una implementación de la interfaz **IMMNotificationClient** .</span><span class="sxs-lookup"><span data-stu-id="641ff-133">The CMMNotificationClient class in the preceding code example is an implementation of the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="641ff-134">Dado **que IMMNotificationClient** se hereda **de IUnknown**, la definición de clase contiene implementaciones de los métodos **IUnknown** **AddRef**, **Release** y **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="641ff-134">Because **IMMNotificationClient** inherits from **IUnknown**, the class definition contains implementations of the **IUnknown** methods **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="641ff-135">Los métodos públicos restantes en la definición de clase son específicos de la interfaz **IMMNotificationClient** .</span><span class="sxs-lookup"><span data-stu-id="641ff-135">The remaining public methods in the class definition are specific to the **IMMNotificationClient** interface.</span></span> <span data-ttu-id="641ff-136">Estos métodos son:</span><span class="sxs-lookup"><span data-stu-id="641ff-136">These methods are:</span></span>

-   <span data-ttu-id="641ff-137">**OnDefaultDeviceChanged**, al que se llama cuando el usuario cambia el rol de dispositivo de un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="641ff-137">**OnDefaultDeviceChanged**, which is called when the user changes the device role of an audio endpoint device.</span></span>
-   <span data-ttu-id="641ff-138">**OnDeviceAdded**, al que se llama cuando el usuario agrega un dispositivo de punto de conexión de audio al sistema.</span><span class="sxs-lookup"><span data-stu-id="641ff-138">**OnDeviceAdded**, which is called when the user adds an audio endpoint device to the system.</span></span>
-   <span data-ttu-id="641ff-139">**OnDeviceRemoved**, al que se llama cuando el usuario quita un dispositivo de punto de conexión de audio del sistema.</span><span class="sxs-lookup"><span data-stu-id="641ff-139">**OnDeviceRemoved**, which is called when the user removes an audio endpoint device from the system.</span></span>
-   <span data-ttu-id="641ff-140">**OnDeviceStateChanged**, al que se llama cuando cambia el estado del dispositivo de un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="641ff-140">**OnDeviceStateChanged**, which is called when the device state of an audio endpoint device changes.</span></span> <span data-ttu-id="641ff-141">(Para obtener más información sobre los Estados de los dispositivos, consulte [constantes de estado de dispositivo \_ \_ XXX](device-state-xxx-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="641ff-141">(For more information about device states, see [DEVICE\_STATE\_ XXX Constants](device-state-xxx-constants.md).)</span></span>
-   <span data-ttu-id="641ff-142">**OnPropertyValueChanged**, al que se llama cuando cambia el valor de una propiedad de un dispositivo de punto de conexión de audio.</span><span class="sxs-lookup"><span data-stu-id="641ff-142">**OnPropertyValueChanged**, which is called when the value of a property of an audio endpoint device changes.</span></span>

<span data-ttu-id="641ff-143">Cada uno de estos métodos toma un parámetro de entrada, *pwstrDeviceId*, que es un puntero a una cadena de identificador de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="641ff-143">Each of these methods takes an input parameter, *pwstrDeviceId*, that is a pointer to an endpoint ID string.</span></span> <span data-ttu-id="641ff-144">La cadena identifica el dispositivo de punto de conexión de audio en el que se produjo el evento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-144">The string identifies the audio endpoint device in which the device event occurred.</span></span>

<span data-ttu-id="641ff-145">En el ejemplo de código anterior, \_ PrintDeviceName es un método privado de la clase CMMNotificationClient que imprime el nombre descriptivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-145">In the preceding code example, \_PrintDeviceName is a private method in the CMMNotificationClient class that prints the friendly name of the device.</span></span> <span data-ttu-id="641ff-146">\_PrintDeviceName toma la cadena del identificador de punto de conexión como parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="641ff-146">\_PrintDeviceName takes the endpoint ID string as an input parameter.</span></span> <span data-ttu-id="641ff-147">Pasa la cadena al método [**IMMDeviceEnumerator:: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="641ff-147">It passes the string to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="641ff-148">**GetDevice** crea un objeto de dispositivo de punto de conexión para representar el dispositivo y proporciona la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="641ff-148">**GetDevice** creates an endpoint device object to represent the device and provides the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface to that object.</span></span> <span data-ttu-id="641ff-149">A continuación, \_ PrintDeviceName llama al método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para recuperar la interfaz **IPropertyStore** en el almacén de propiedades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-149">Next, \_PrintDeviceName calls the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to retrieve the **IPropertyStore** interface to the device's property store.</span></span> <span data-ttu-id="641ff-150">Por último, \_ PrintDeviceName llama al método **IPropertyStore:: GetItem** para obtener la propiedad de nombre descriptivo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="641ff-150">Finally, \_PrintDeviceName calls the **IPropertyStore::GetItem** method to obtain the friendly-name property of the device.</span></span> <span data-ttu-id="641ff-151">Para obtener más información sobre **IPropertyStore**, consulte la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="641ff-151">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="641ff-152">Además de los eventos de dispositivo, los clientes pueden registrarse para recibir notificaciones de eventos de sesión de audio y eventos de volumen de punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="641ff-152">In addition to device events, clients can register to receive notifications of audio-session events and endpoint-volume events.</span></span> <span data-ttu-id="641ff-153">Para obtener más información, vea [**interfaz IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) y [**interfaz IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span><span class="sxs-lookup"><span data-stu-id="641ff-153">For more information, see [**IAudioSessionEvents Interface**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) and [**IAudioEndpointVolumeCallback Interface**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="641ff-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="641ff-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="641ff-155">Dispositivos de punto de conexión de audio</span><span class="sxs-lookup"><span data-stu-id="641ff-155">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> </dl>

 

 



