---
description: Roles de dispositivo para DirectShow aplicaciones
ms.assetid: 54f42bda-b4a0-465c-9ce6-9102d2908776
title: Roles de dispositivo para DirectShow aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e22a86e5537f11b6b4153753841a2682b5ac77a043a3fa74538714a2540377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957364"
---
# <a name="device-roles-for-directshow-applications"></a>Roles de dispositivo para DirectShow aplicaciones

> [!Note]  
> MMDevice [API admite roles](mmdevice-api.md) de dispositivo. Sin embargo, la interfaz de usuario Windows Vista no implementa compatibilidad con esta característica. La compatibilidad de la interfaz de usuario con los roles de dispositivo podría implementarse en una versión futura de Windows. Para obtener más información, vea [Roles de dispositivo en Windows Vista](device-roles-in-windows-vista.md).

 

La API DirectShow no proporciona un medio para que una aplicación seleccione el dispositivo de punto de conexión de [audio](audio-endpoint-devices.md) asignado a un rol de [dispositivo determinado.](device-roles.md) Sin embargo, Windows Vista, las API de audio principales se pueden usar junto con una aplicación DirectShow para habilitar la selección de dispositivos en función del rol de dispositivo. Con la ayuda de las API de audio principales, la aplicación puede:

-   Identifique el dispositivo de punto de conexión de audio que el usuario ha asignado a un rol de dispositivo determinado.
-   Cree un DirectShow de representación de audio con una [**interfaz IBaseFilter**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) que encapsula el dispositivo de punto de conexión de audio.
-   Cree un DirectShow gráfico que incorpore el filtro.

Para obtener más información sobre DirectShow [**e IBaseFilter,**](/windows/desktop/api/strmif/nn-strmif-ibasefilter)consulte la documentación Windows SDK.

En el ejemplo de código siguiente se muestra cómo crear un filtro de representación de audio DirectShow que encapsula el dispositivo del punto de conexión de representación asignado a un rol de dispositivo determinado:


```C++
//-----------------------------------------------------------
// Create a DirectShow audio rendering filter that
// encapsulates the audio endpoint device that is currently
// assigned to the specified device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

// This application's audio session GUID
const GUID guidAudioSessionId = {
    0xb13ff52e, 0xa5cf, 0x4fca,
    {0x9f, 0xc3, 0x42, 0x26, 0x5b, 0x0b, 0x14, 0xfb}
};

HRESULT CreateAudioRenderer(ERole role, IBaseFilter** ppAudioRenderer)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    if (ppAudioRenderer == NULL)
    {
        return E_POINTER;
    }

    // Activate the IBaseFilter interface on the
    // audio renderer with the specified role.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator,
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    DIRECTX_AUDIO_ACTIVATION_PARAMS  daap;
    daap.cbDirectXAudioActivationParams = sizeof(daap);
    daap.guidAudioSession = guidAudioSessionId;
    daap.dwAudioStreamFlags = AUDCLNT_STREAMFLAGS_CROSSPROCESS;

    PROPVARIANT  var;
    PropVariantInit(&var);

    var.vt = VT_BLOB;
    var.blob.cbSize = sizeof(daap);
    var.blob.pBlobData = (BYTE*)&daap;

    hr = pDevice->Activate(__uuidof(IBaseFilter),
                           CLSCTX_ALL, &var,
                           (void**)ppAudioRenderer);
    EXIT_ON_ERROR(hr)

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    return hr;
}
```



En el ejemplo de código anterior, la función CreateAudioRenderer acepta un rol de dispositivo (eConsole, eMultimedia o eCommunications) como parámetro de entrada. El segundo parámetro es un puntero a través del cual la función escribe la dirección de una instancia de [**interfaz IBaseFilter.**](/windows/desktop/api/strmif/nn-strmif-ibasefilter) Además, en el ejemplo se muestra cómo usar el método [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para asignar la secuencia de audio de la instancia de **IBaseFilter** a una sesión de audio entre procesos con un GUID de sesión específico de la aplicación (especificado por la **constante guidAudioSessionId).** El tercer parámetro de la llamada **a Activate** apunta a una estructura que contiene el GUID de sesión y la marca de proceso cruzado. Si el usuario ejecuta varias instancias de la aplicación, las secuencias de audio de todas las instancias usan el mismo GUID de sesión y, por tanto, pertenecen a la misma sesión.

Como alternativa, el autor de la llamada puede especificar **NULL** como tercer parámetro en la llamada [**Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) para asignar la secuencia a la sesión predeterminada como sesión específica del proceso con el VALOR GUID de sesión \_ NULL. Para obtener más información, **vea IMMDevice::Activate**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
