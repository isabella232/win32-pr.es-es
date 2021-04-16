---
description: Streaming audio renderer (SAR) es un receptor de medios que representa el audio.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Representador de audio de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696674"
---
# <a name="streaming-audio-renderer"></a>Representador de audio de streaming

Streaming audio renderer (SAR) es un receptor de medios que representa el audio. Cada instancia de SAR representa una secuencia de audio única. Para representar varias secuencias, use varias instancias del SAR.

Para crear el SAR, llame a una de las siguientes funciones:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer). Devuelve un puntero al SAR.
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate). Devuelve un puntero a un objeto de activación, que se puede usar para crear el SAR.

La segunda función, que devuelve un objeto de activación, es necesaria si se está reproduciendo contenido protegido, ya que el objeto de activación se debe serializar en el proceso protegido. En el caso de contenido sin cifrar, puede usar cualquiera de las dos funciones.

El SAR puede recibir audio sin comprimir en formato de punto flotante de PCM o IEEE. Si la velocidad de reproducción es mayor o menor que 1 ×, el SAR ajusta automáticamente el paso.

## <a name="configuring-the-audio-renderer"></a>Configuración del representador de audio

El SAR admite varios atributos de configuración. El mecanismo para establecer estos atributos depende de la función a la que llame para crear el SAR. Si usa la función [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) , haga lo siguiente:

1.  Cree un nuevo almacén de atributos mediante una llamada a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Agregue los atributos al almacén de atributos.
3.  Pase el almacén de atributos a la función [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) en el parámetro *pAudioAttributes* .

Si usa la función [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) , la función devuelve un puntero a la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) en el parámetro *ppActivate* . Utilice este puntero para agregar los atributos.

Para obtener una lista de atributos de configuración, vea [atributos de representador de audio](audio-renderer-attributes.md).

## <a name="selecting-the-audio-endpoint-device"></a>Selección del dispositivo de extremo de audio

Un *dispositivo de punto de conexión de audio* es un dispositivo de hardware que representa o captura audio. Algunos ejemplos son los altavoces, los auriculares, los micrófonos y los reproductores de CD. SAR siempre usa un dispositivo de representación de audio. Hay dos maneras de seleccionar el dispositivo.

El primer enfoque consiste en enumerar los dispositivos de representación de audio en el sistema mediante la interfaz [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Esta interfaz se documenta en la documentación básica de la API de audio.

1.  Cree el objeto de enumerador de dispositivos.
2.  Use el enumerador de dispositivos para enumerar los dispositivos de representación de audio. Cada dispositivo se representa mediante un puntero a la interfaz [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .
3.  Seleccione un dispositivo, en función de las propiedades del dispositivo o la selección del usuario.
4.  Llame a [**IMMDevice:: getId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obtener el identificador de dispositivo.
5.  Establezca el identificador de dispositivo como el valor del atributo de ID. de [**\_ extremo de \_ atributo de representador \_ \_ \_ de audio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .

En lugar de enumerar los dispositivos, puede especificar el dispositivo de audio por su *rol*. Un rol de audio identifica una categoría general de uso. Por ejemplo, el rol de *consola* se define para juegos y notificaciones del sistema, mientras que el rol *multimedia* se define para música y películas. Cada rol tiene un dispositivo de representación de audio asignado y el usuario puede cambiar estas asignaciones. Si especifica un rol de dispositivo, el SAR usa cualquier dispositivo de audio que se haya asignado para ese rol. Para especificar el rol de dispositivo, establezca el atributo de [**\_ rol de punto de conexión de \_ atributo de representador \_ \_ \_ de audio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .

Los dos atributos que se enumeran en esta sección son mutuamente excluyentes. Si no establece ninguno de ellos, el SAR usa el dispositivo de audio que está asignado al rol **eConsole** .

En el código siguiente se enumeran los dispositivos de representación de audio y se asigna el primer dispositivo de la lista al SAR. En este ejemplo se usa la función [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) para crear el SAR.


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



Para crear el objeto de activación para el SAR, cambie el código que aparece después de la llamada a [**IMMDevice:: getId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) a lo siguiente:


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



## <a name="selecting-the-audio-session"></a>Seleccionar la sesión de audio

Una sesión de audio es un grupo de secuencias de audio relacionadas que una aplicación puede administrar colectivamente. La aplicación puede controlar el nivel de volumen y silenciar el estado de cada sesión. Las sesiones se identifican mediante un GUID. Para especificar la sesión de audio para el SAR, use el atributo de ID. de [ \_ sesión de \_ atributo del representador \_ \_ \_ de audio MF](mf-audio-renderer-attribute-session-id-attribute.md) . Si no se establece este atributo, el SAR se une a la sesión predeterminada para ese proceso, identificado por el **GUID \_ null**.

De forma predeterminada, una sesión de audio es específica del proceso, lo que significa que solo contiene flujos del proceso de llamada. Para unirse a una sesión entre procesos, establezca el atributo [MF \_ audio \_ renderer Attribute \_ \_ Flags](mf-audio-renderer-attribute-flags-attribute.md) con el valor **MF \_ audio \_ renderer \_ Attribute \_ Flags \_ CROSSPROCESS**.

Después de crear el SAR, use la interfaz [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) para unir la sesión a un grupo de sesiones, todas las cuales están controladas por el mismo control de volumen en el panel de control. También puede usar esta interfaz para establecer el nombre para mostrar y el icono que aparece en el control de volumen.

## <a name="controlling-volume-levels"></a>Controlar los niveles de volumen

Para controlar el nivel de volumen maestro de todas las secuencias de la sesión de audio de SAR, use la interfaz [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) . Para controlar el volumen de una secuencia individual, o para controlar el volumen de canales individuales dentro de una secuencia, use la interfaz [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) . Ambas interfaces se obtienen mediante una llamada a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). Puede llamar a **GetService** directamente en el SAR o llamarlo en la sesión multimedia. Los niveles de volumen se expresan como valores de atenuación. Para cada canal, el nivel de atenuación es el producto del volumen maestro y el volumen del canal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> </dl>

 

 
