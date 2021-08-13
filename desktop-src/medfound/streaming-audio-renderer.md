---
description: El representador de audio de streaming (SAR) es un receptor multimedia que representa audio.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Representador de audio de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01752cbec7d801177b39d939baeca93f720e12aafeaf9845c1aa0ded033c3fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238270"
---
# <a name="streaming-audio-renderer"></a>Representador de audio de streaming

El representador de audio de streaming (SAR) es un receptor multimedia que representa audio. Cada instancia de la RAE representa una sola secuencia de audio. Para representar varias secuencias, use varias instancias de la SAR.

Para crear la SAR, llame a cualquiera de las siguientes funciones:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer). Devuelve un puntero a la SAR.
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate). Devuelve un puntero a un objeto de activación, que se puede usar para crear la SAR.

La segunda función, que devuelve un objeto de activación, es necesaria si se reproduce contenido protegido, porque el objeto de activación se debe serializar al proceso protegido. Para borrar contenido, puede usar cualquiera de las funciones.

La SAR puede recibir audio sin comprimir en formato de punto flotante PCM o IEEE. Si la velocidad de reproducción es más rápida o más lenta que 1×, la RAE ajusta automáticamente el tono.

## <a name="configuring-the-audio-renderer"></a>Configuración del representador de audio

La SAR admite varios atributos de configuración. El mecanismo para establecer estos atributos depende de la función a la que llame para crear la SAR. Si usa la [**función MFCreateAudioRenderer,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) haga lo siguiente:

1.  Cree un nuevo almacén de atributos mediante una [**llamada a MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Agregue los atributos al almacén de atributos.
3.  Pase el almacén de atributos a [**la función MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) en el *parámetro pAudioAttributes.*

Si usa la función [**MFCreateAudioRendererActivate,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) la función devuelve un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) en el *parámetro ppActivate.* Use este puntero para agregar los atributos.

Para obtener una lista de atributos de configuración, vea [Atributos del representador de audio.](audio-renderer-attributes.md)

## <a name="selecting-the-audio-endpoint-device"></a>Selección del dispositivo de punto de conexión de audio

Un *dispositivo de punto de conexión* de audio es un dispositivo de hardware que representa o captura audio. Algunos ejemplos son altavoces, auriculares, micrófonos y reproductores de CD. La RAE siempre usa un dispositivo de representación de audio. Hay dos maneras de seleccionar el dispositivo.

El primer enfoque es enumerar los dispositivos de representación de audio en el sistema mediante la [**interfaz IMMDeviceEnumerator.**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Esta interfaz se documenta en la documentación de la API de audio principal.

1.  Cree el objeto enumerador de dispositivos.
2.  Use el enumerador de dispositivos para enumerar los dispositivos de representación de audio. Cada dispositivo se representa mediante un puntero a la [**interfaz IMMDevice.**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
3.  Seleccione un dispositivo, en función de las propiedades del dispositivo o de la selección del usuario.
4.  Llame [**a IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener el identificador del dispositivo.
5.  Establezca el identificador de dispositivo como el valor del atributo [**MF \_ AUDIO \_ RENDERER ATTRIBUTE ENDPOINT \_ \_ \_ ID.**](mf-audio-renderer-attribute-endpoint-id-attribute.md)

En lugar de enumerar dispositivos, puede especificar el dispositivo de audio por su *rol*. Un rol de audio identifica una categoría general de uso. Por ejemplo, el *rol de consola* se define para juegos y notificaciones del sistema, mientras que el rol *multimedia* se define para música y películas. Cada rol tiene asignado un dispositivo de representación de audio y el usuario puede cambiar estas asignaciones. Si especifica un rol de dispositivo, la RAE usa cualquier dispositivo de audio que se haya asignado para ese rol. Para especificar el rol de dispositivo, establezca el atributo [**MF \_ AUDIO \_ RENDERER ATTRIBUTE ENDPOINT \_ \_ \_ ROLE.**](mf-audio-renderer-attribute-endpoint-role-attribute.md)

Los dos atributos enumerados en esta sección son mutuamente excluyentes. Si no establece ninguno de ellos, la RAE usa el dispositivo de audio asignado al **rol eConsole.**

El código siguiente enumera los dispositivos de representación de audio y asigna el primer dispositivo de la lista a la RAE. En este ejemplo se [**usa la función MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) para crear la SAR.


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



Para crear el objeto de activación para la RAE, cambie el código que aparece después de la llamada a [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) por lo siguiente:


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a>Selección de la sesión de audio

Una sesión de audio es un grupo de secuencias de audio relacionadas que una aplicación puede administrar colectivamente. La aplicación puede controlar el nivel de volumen y el estado de exclusión mutua de cada sesión. Las sesiones se identifican mediante GUID. Para especificar la sesión de audio para la RAE, use el atributo [MF \_ AUDIO \_ RENDERER ATTRIBUTE SESSION \_ \_ \_ ID.](mf-audio-renderer-attribute-session-id-attribute.md) Si no establece este atributo, la SAR une la sesión predeterminada para ese proceso, identificada por **GUID \_ NULL**.

De forma predeterminada, una sesión de audio es específica del proceso, lo que significa que solo contiene secuencias del proceso de llamada. Para unir una sesión entre procesos, establezca el atributo [MF \_ AUDIO \_ RENDERER ATTRIBUTE \_ \_ FLAGS](mf-audio-renderer-attribute-flags-attribute.md) con el valor **MF AUDIO \_ \_ RENDERER ATTRIBUTE \_ \_ FLAGS \_ CROSSPROCESS**.

Después de crear la SAR, use la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) para unir la sesión a un grupo de sesiones, todas controladas por el mismo control de volumen en el panel de control. También puede usar esta interfaz para establecer el nombre para mostrar y el icono que aparecen en el control de volumen.

## <a name="controlling-volume-levels"></a>Controlar los niveles de volumen

Para controlar el nivel de volumen maestro de todas las secuencias de la sesión de audio de la SAR, use la interfaz [**IMFSimpleAudioVolume.**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) Para controlar el volumen de una secuencia individual, o para controlar el volumen de canales individuales dentro de una secuencia, use la interfaz [**IMFAudioStreamVolume.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) Ambas interfaces se obtienen mediante una llamada [**a IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). Puede llamar a **GetService** directamente en la SAR o llamarlo en la sesión multimedia. Los niveles de volumen se expresan como valores de atenuación. Para cada canal, el nivel de atenuación es el producto del volumen maestro y el volumen del canal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> </dl>

 

 
