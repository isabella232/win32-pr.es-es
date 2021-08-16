---
description: Roles de dispositivo para aplicaciones multimedia Windows heredadas
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: Roles de dispositivo para aplicaciones multimedia Windows heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b0c1c8b61da896ca8877a913ba14d5013de71ac6fd7c14bcdebfe21c4ffcb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406925"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a>Roles de dispositivo para aplicaciones multimedia Windows heredadas

> [!Note]  
> MMDevice API admite roles de dispositivo. Sin embargo, la interfaz de usuario Windows Vista no implementa compatibilidad con esta característica. La compatibilidad de la interfaz de usuario con los roles de dispositivo podría implementarse en una versión futura de Windows. Para obtener más información, vea [Roles de dispositivo en Windows Vista](device-roles-in-windows-vista.md).

 

Las funciones Windows **waveOutXxx** y **waveInXxx** multimedia no proporcionan ningún medio para que una aplicación seleccione el dispositivo de punto de conexión de [audio](audio-endpoint-devices.md) que el usuario ha asignado a un rol de dispositivo [determinado.](device-roles.md) Sin embargo, Windows Vista, las API de audio principales se pueden usar junto con una aplicación multimedia Windows para habilitar la selección de dispositivos en función del rol del dispositivo. Por ejemplo, con la ayuda de [la API MMDevice](mmdevice-api.md), una aplicación **waveOutXxx** puede identificar el dispositivo de punto de conexión de audio asignado a un rol, identificar el dispositivo de salida de forma de onda correspondiente y llamar a la función **waveOutOpen** para abrir una instancia del dispositivo. Para obtener más información sobre **waveOutXxx** y **waveInXxx,** consulte la documentación Windows SDK.

En el ejemplo de código siguiente se muestra cómo obtener el identificador de dispositivo de forma de onda para el dispositivo de punto de conexión de representación asignado a un rol de dispositivo determinado:


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



En el ejemplo de código anterior, la función GetWaveOutId acepta un rol de dispositivo (eConsole, eMultimedia o eCommunications) como parámetro de entrada. El segundo parámetro es un puntero a través del cual la función escribe el identificador de dispositivo de forma de onda para el dispositivo de salida de forma de onda asignado al rol especificado. A continuación, la aplicación puede **llamar a waveOutOpen** con este identificador para abrir el dispositivo.

El bucle main del ejemplo de código anterior contiene dos llamadas a la **función waveOutMessage.** La primera llamada envía un mensaje DRV QUERYFUNCTIONINSTANCEIDSIZE para recuperar el tamaño, en bytes, de la cadena de identificador de punto de conexión del dispositivo de onda identificado por el \_ *parámetro waveOutId.* [](endpoint-id-strings.md) (La cadena de identificador de punto de conexión identifica el dispositivo de punto de conexión de audio que subyace a la abstracción del dispositivo de forma de onda). El tamaño notificado por esta llamada incluye el espacio para el carácter nulo final al final de la cadena. El programa puede usar la información de tamaño para asignar un búfer lo suficientemente grande como para contener toda la cadena de identificador de punto de conexión.

La segunda llamada a **waveOutMessage** envía un mensaje QUERYFUNCTIONINSTANCEID de DRV para recuperar la cadena de identificador de dispositivo del dispositivo de salida \_ de forma de onda. El código de ejemplo compara esta cadena con la cadena de identificador de dispositivo del dispositivo de punto de conexión de audio con el rol de dispositivo especificado. Si las cadenas coinciden, la función escribe el identificador de dispositivo de forma de onda en la ubicación a la que apunta el *parámetro pWaveOutId*. El autor de la llamada puede usar este identificador para abrir el dispositivo de salida de forma de onda que tiene el rol de dispositivo especificado.

Windows Vista admite los mensajes DRV \_ QUERYFUNCTIONINSTANCEIDSIZE y DRV \_ QUERYFUNCTIONINSTANCEID. No se admiten en versiones anteriores de Windows, incluidos Windows Server 2003, Windows XP y Windows 2000.

La función del ejemplo de código anterior obtiene el identificador de dispositivo de forma de onda para un dispositivo de representación, pero, con algunas modificaciones, se puede adaptar para obtener el identificador de dispositivo de forma de onda para un dispositivo de captura. A continuación, la aplicación puede llamar **a waveInOpen** con este identificador para abrir el dispositivo. Para cambiar el ejemplo de código anterior para obtener el identificador de dispositivo de forma de onda para el dispositivo de punto de conexión de captura de audio asignado a un rol determinado, haga lo siguiente:

-   Reemplace todas las llamadas **a la función waveOutXxx** en el ejemplo anterior por las llamadas de función **waveInXxx** correspondientes.
-   Cambie el tipo de identificador HWAVEOUT a HWAVEIN.
-   Reemplace la constante de enumeración [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) eRender por eCapture.

En Windows Vista, las funciones **waveOutOpen** y **waveInOpen** siempre asignan las secuencias de audio que crean a la sesión predeterminada, la sesión específica del proceso identificada por el VALOR GUID de la sesión \_ NULL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



