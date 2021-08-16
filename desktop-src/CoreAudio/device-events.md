---
description: Eventos de dispositivo
ms.assetid: b31500d6-a79d-4e6e-878e-6bd77055f1ad
title: Eventos de dispositivo (API de audio principales)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61538bd7d8d297b52a321f446bb11c3e1365e549a3c2947b55538730c1660c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407033"
---
# <a name="device-events-core-audio-apis"></a>Eventos de dispositivo (API de audio principales)

Un evento de dispositivo notifica a los clientes un cambio en el estado de un dispositivo de punto de [conexión de audio](audio-endpoint-devices.md) en el sistema. A continuación se muestran ejemplos de eventos de dispositivo:

-   El usuario habilita o deshabilita un dispositivo de punto de conexión de audio desde Administrador de dispositivos o desde el panel de control multimedia Windows, Mmsys.cpl.
-   El usuario agrega un adaptador de audio al sistema o quita un adaptador de audio del sistema.
-   El usuario conecta un dispositivo de punto de conexión de audio a un conector de audio con detección de presencia de conector o quita un dispositivo de punto de conexión de audio de dicho conector.
-   El usuario cambia el [rol de dispositivo](device-roles.md) asignado a un dispositivo.
-   Cambia el valor de [una propiedad de un](device-properties.md) dispositivo.

La adición o eliminación de un adaptador de audio genera eventos de dispositivo para todos los dispositivos de punto de conexión de audio que se conectan al adaptador. Los cuatro primeros elementos de la lista anterior son ejemplos de cambios en el estado del dispositivo. Para obtener más información sobre los estados del dispositivo de los dispositivos de punto de conexión de audio, vea [DEVICE \_ STATE XXX \_ Constants](device-state-xxx-constants.md). Para obtener más información sobre la detección de presencia de conector, vea [Dispositivos de punto de conexión de audio.](audio-endpoint-devices.md)

Un cliente puede registrarse para recibir una notificación cuando se produzcan eventos de dispositivo. En respuesta a estas notificaciones, el cliente puede cambiar dinámicamente la forma en que usa un dispositivo determinado o seleccionar otro dispositivo para usarlo para un propósito determinado.

Por ejemplo, si una aplicación reproduce una pista de audio a través de un conjunto de altavoces USB y el usuario desconecta los altavoces del conector USB, la aplicación recibe una notificación de evento de dispositivo. En respuesta al evento, si la aplicación detecta que un conjunto de altavoces de escritorio está conectado al adaptador de audio integrado en la placa base del sistema, la aplicación puede reanudar la reproducción de la pista de audio a través de los altavoces de escritorio. En este ejemplo, la transición de los altavoces USB a los altavoces de escritorio se produce automáticamente, sin necesidad de que el usuario intervenga mediante la redirección explícita de la aplicación.

Para registrarse para recibir notificaciones de dispositivo, un cliente llama al método [**IMMDeviceEnumerator::RegisterEndpointNotificationCallback.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-registerendpointnotificationcallback) Cuando el cliente ya no requiere notificaciones, las cancela llamando al método [**IMMDeviceEnumerator::UnregisterEndpointNotificationCallback.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-unregisterendpointnotificationcallback) Ambos métodos toman un parámetro de entrada, denominado *pNotify*, que es un puntero a una instancia de interfaz [**IMMNotificationClient.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)

Un cliente implementa la interfaz **IMMNotificationClient.** La interfaz contiene varios métodos, cada uno de los cuales actúa como rutina de devolución de llamada para un tipo determinado de evento de dispositivo. Cuando se produce un evento de dispositivo en un dispositivo de punto de conexión de audio, el módulo MMDevice llama al método adecuado en la interfaz **IMMNotificationClient** de cada cliente que está registrado actualmente para recibir notificaciones de eventos de dispositivo. Estas llamadas pasan una descripción del evento a los clientes. Para obtener más información, [**vea IMMNotificationClient (Interfaz).**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient)

Un cliente registrado para recibir notificaciones de eventos de dispositivo recibirá notificaciones de todos los tipos de eventos de dispositivo que se producen en todos los dispositivos de punto de conexión de audio del sistema. Si un cliente solo está interesado en determinados tipos de eventos o en determinados dispositivos, los métodos de su implementación **IMMNotificationClient** deben filtrar los eventos correctamente.

El SDK Windows proporciona ejemplos que incluyen varias implementaciones para la [**interfaz IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient). Para más información, consulte [Ejemplos de SDK que usan las API de audio principales.](sdk-samples-that-use-the-core-audio-apis.md)

En el ejemplo de código siguiente se muestra una posible implementación de la **interfaz IMMNotificationClient:**


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



La clase CMMNotificationClient del ejemplo de código anterior es una implementación de la **interfaz IMMNotificationClient.** Dado **que IMMNotificationClient** hereda de **IUnknown,** la definición de clase contiene implementaciones de los métodos **IUnknown** **AddRef,** **Release** y **QueryInterface**. Los métodos públicos restantes de la definición de clase son específicos de **la interfaz IMMNotificationClient.** Estos métodos son:

-   **OnDefaultDeviceChanged**, al que se llama cuando el usuario cambia el rol de dispositivo de un dispositivo de punto de conexión de audio.
-   **OnDeviceAdded**, al que se llama cuando el usuario agrega un dispositivo de punto de conexión de audio al sistema.
-   **OnDeviceRemoved**, al que se llama cuando el usuario quita un dispositivo de punto de conexión de audio del sistema.
-   **OnDeviceStateChanged**, al que se llama cuando cambia el estado del dispositivo de un punto de conexión de audio. (Para obtener más información sobre los estados del dispositivo, vea DEVICE STATE XXX Constants [Constantes [XXX de ESTADO DEL \_ \_ DISPOSITIVO]).](device-state-xxx-constants.md)
-   **OnPropertyValueChanged**, al que se llama cuando cambia el valor de una propiedad de un dispositivo de punto de conexión de audio.

Cada uno de estos métodos toma un parámetro de entrada, *pwstrDeviceId*, que es un puntero a una cadena de identificador de punto de conexión. La cadena identifica el dispositivo de punto de conexión de audio en el que se produjo el evento del dispositivo.

En el ejemplo de código anterior, PrintDeviceName es un método privado de la clase CMMNotificationClient que imprime el nombre \_ descriptivo del dispositivo. \_PrintDeviceName toma la cadena de identificador de punto de conexión como parámetro de entrada. Pasa la cadena al método [**IMMDeviceEnumerator::GetDevice.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) **GetDevice** crea un objeto de dispositivo de punto de conexión para representar el dispositivo y proporciona la [**interfaz IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) a ese objeto. A \_ continuación, PrintDeviceName llama al método [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para recuperar la **interfaz IPropertyStore** en el almacén de propiedades del dispositivo. Por último, \_ PrintDeviceName llama al **método IPropertyStore::GetItem** para obtener la propiedad de nombre descriptivo del dispositivo. Para obtener más información sobre **IPropertyStore,** consulte la documentación Windows SDK.

Además de los eventos de dispositivo, los clientes pueden registrarse para recibir notificaciones de eventos de sesión de audio y eventos de volumen de punto de conexión. Para obtener más información, [**vea IAudioSessionEvents Interface**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) e [**IAudioEndpointVolumeCallback Interface**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)
</dt> </dl>

 

 



