---
description: Core Audio API se introdujo en Windows Vista, que proporcionaba un nuevo conjunto de componentes de audio en modo de usuario que una aplicación cliente puede usar para representar o capturar secuencias de audio con funcionalidades de audio mejoradas.
ms.assetid: eb99c266-16d2-4a14-bc1d-059a0a94db13
title: Novedades de core audio API en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6160b275512a7efbd3b795e263f2ce8ae01be965
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164757"
---
# <a name="whats-new-for-core-audio-apis-in-windows-7"></a>Novedades de core audio API en Windows 7

Core Audio API se introdujo en Windows Vista, que proporcionaba un nuevo conjunto de componentes de audio en modo de usuario que una aplicación cliente puede usar para representar o capturar secuencias de audio con funcionalidades de audio mejoradas. Para obtener información general sobre este conjunto de API, consulte [Acerca de Windows Core Audio API](about-the-windows-core-audio-apis.md).

Las API de audio principales se han mejorado en Windows 7. En la tabla siguiente se resumen las nuevas características y las mejoras de core Audio API:




| Característica | Descripción | 
|---------|-------------|
| Mejoras genéricas | Las siguientes características se han mejorado en Windows 7:<ul><li>En Windows 7 secuencias de modo compartido se ejecutan <em>en modo de baja latencia</em>. El motor de audio se ejecuta en modo de extracción con una reducción significativa de la latencia. Esto es muy útil para las aplicaciones de comunicación que requieren una latencia de secuencia de audio baja para un streaming más rápido.</li><li>Windows 7 proporciona una mejor detección de roles de dispositivo cuando se agrega un nuevo dispositivo al sistema. Para obtener más información, vea <a href="device-roles-in-windows-vista.md">Trabajar con roles de dispositivo.</a></li><li>En Windows 7 puede escuchar música desde el reproductor multimedia portátil a través de los altavoces del equipo. Puede usar esta característica del Monitor de captura conectando un reproductor multimedia portátil al equipo con un cable de audio análogo. En el pasado, algunos OEM han proporcionado esta funcionalidad en el controlador de audio mediante un bucle de recuperación de hardware. En Windows 7, esta funcionalidad se ha agregado al sistema operativo. Dado que esto está en el sistema y no en el controlador, puede usarlo para cualquier otro dispositivo conectado al sistema, como un casco USB.</li><li>El audio HDMI se ha mejorado en Windows 7, que proporciona compatibilidad con el formato de alta velocidad de bits. Con esta mejora, puede admitir formatos de audio multicanal y de audio comprimido a través de un conector HDMI a un receptor de audio.</li><li>En Windows Vista, Reproductor de Windows Media reproducir música solo a través del dispositivo de audio predeterminado, que el usuario no puede cambiar. Para Reproductor de Windows Media representar audio en un dispositivo determinado, el dispositivo predeterminado debe cambiarse en el panel de control <strong>Sonidos.</strong> En Windows 7, Reproductor de Windows Media proporciona API que permiten que una aplicación se represente en cualquier dispositivo seleccionado por el usuario y no solo en el dispositivo predeterminado.</li><li>En Windows Vista, si un equipo que reproduce audio cambia al modo de ahorro de energía, el equipo está bloqueado y, si el usuario desea interrumpir la reproducción, el usuario debe iniciar sesión y presionar la tecla de detección para detener la reproducción. En Windows 7, si el equipo está bloqueado, todavía puede controlar la reproducción mediante el control HID en el teclado.</li><li>Windows 7 reduce el consumo de energía para cualquier aplicación que use DirectSound y DirectShow para representar medios. Además, el servicio Programador de clases multimedia habilita el audio resistente a problemas y usa menos energía mientras se generan las muestras de audio.</li></ul> | 
| Dispositivo de comunicación (nuevo) | En esta versión se ha agregado un nuevo tipo de dispositivo al panel de control <strong>Sonidos:</strong> <strong>Dispositivo de</strong> comunicaciones. Este dispositivo se usa principalmente para las comunicaciones, es decir, para realizar o recibir llamadas telefónicas en el equipo. Una aplicación de comunicación puede usar componentes de Core Audio para obtener una referencia al punto de conexión del dispositivo de comunicación predeterminado y representar secuencias de audio con fines de comunicación. El sistema operativo considera que la secuencia abierta en un dispositivo de comunicación es un flujo de comunicación. Las operaciones WASAPI en una secuencia de comunicación son similares a cualquier otra secuencia de audio. Para obtener más información, vea <a href="device-roles-in-windows-vista.md">Trabajar con roles de dispositivo.</a> | 
| Atenuación de secuencias o afijo de audio (nuevo) | El agachamiento automático o <a href="stream-attenuation.md">atenuación</a> de secuencias es una nueva característica de Windows 7 que está pensada para aplicaciones voIP y de comunicación unificada. De forma predeterminada, el sistema operativo reduce la intensidad de una secuencia de audio cuando se recibe una secuencia de comunicación, como una llamada de teléfono, en el dispositivo de comunicación a través del equipo. El usuario establece las opciones de volumen en el panel <strong>de</strong> control Sonido. Se han agregado nuevas API en el SDK de Windows que permiten a las aplicaciones reemplazar el comportamiento predeterminado de omisión. Para obtener más información sobre cómo implementar una característica de afijo personalizado, vea <a href="providing-a-custom-ducking-experience.md">Proporcionar un comportamiento de afijo personalizado.</a> <br /> | 
| Enrutamiento de secuencias (nuevo) | En Windows 7, las API de audio principales se han mejorado para transferir una secuencia de audio sin problemas desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado. Los conjuntos de API de audio de alto nivel que usan Core Audio API, como las API Media Foundation, Direct Sound y WAVE, implementan la característica de enrutamiento de secuencias. Las aplicaciones multimedia que usan estos conjuntos de API para reproducir o capturar una secuencia usan la implementación predeterminada y no tienen que modificar la aplicación. Sin embargo, si la aplicación multimedia usa las API core audio directamente, la aplicación debe proporcionar la implementación de enrutamiento de secuencias. Para ello, la aplicación debe controlar los nuevos eventos que se han agregado que notifican a un cliente WASAPI cuando el dispositivo predeterminado está conectado o quitado. Para obtener más información sobre esta característica, vea <a href="stream-routing.md">Stream Routing</a>. | 
| Audio en modo de usuario protegido (IAM) (mejorado) | SE HA actualizado para Windows 7 para proporcionar las siguientes características:<ul><li>Establecer bits del sistema de administración de copia serie (SCMS) en puntos de conexión S/PDIF y bits de digital Content Protection de ancho de banda alto (HDCP) en puntos de conexión de High-Definition Multimedia Interface (HDMI).</li><li>Habilitar controles de protección SCMS y HDMI fuera de un entorno protegido (PE).</li></ul>Para obtener más información sobre las mejoras, vea <a href="protected-user-mode-audio--puma-.md">Audio en modo de usuario protegido (IAM).</a><br /> | 
| La <strong>estructura DESATEXTENSIBLE</strong> se ha ampliado a <strong>la WAVEFORMATEXTENSIBLE_IEC61937</strong> estructura (Nuevo) | En Windows 7, se ha agregado una nueva estructura para admitir las transmisiones IEC 61937. <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> extiende la estructura <strong>DESATEXTENSIBLE para</strong> almacenar dos conjuntos de características de secuencia de audio: el formato de audio codificado antes de la transmisión y las características de la secuencia de audio después de que se haya descodificado. La nueva estructura especifica explícitamente el número efectivo de canales, el tamaño de la muestra y la velocidad de datos de un formato que no es PCM. Con esta información, una aplicación puede deducir el nivel de calidad de la secuencia que no es PCM después de que se descomprima y se reproduce. Para obtener más información, vea <a href="representing-formats-for-iec-61937-transmissions.md">Representar formatos para transmisiones IEC 61937.</a><br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient::Initialize</strong></a> (mejorado) | El <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>método IAudioClient::Initialize</strong></a> se ha mejorado para indicar errores específicos que pueden producirse al abrir una secuencia de audio. Los nuevos códigos de error son:<ul><li>AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED</li><li>AUDCLNT_E_BUFFER_SIZE_ERROR</li><li>AUDCLNT_E_INVALID_DEVICE_PERIOD</li></ul>Para obtener más información sobre estos errores, vea la sección Valor devuelto <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>de IAudioClient::Initialize</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient::GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient::GetBuffer</strong></a> (mejorado) | Los métodos <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient::GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient::GetBuffer</strong></a> se han mejorado para devolver el código de error de AUDCLNT_E_BUFFER_ERROR que indica que no se recuperó el búfer del punto de conexión en el modo exclusivo. Para obtener más información, vea Comentarios en <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient::GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient::GetBuffer</strong></a>. | 
| Funcionalidad de detección de conectores (mejorada) | Una nueva interfaz en Windows 7, <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2"><strong>IKsJackDescription2</strong></a>, extiende <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription"><strong>IKs JackDescription</strong></a>. Con la nueva interfaz, la pila de audio o una aplicación pueden obtener información adicional sobre el conector. Esto incluye la funcionalidad de detección del conector y si el formato del dispositivo ha cambiado dinámicamente. | 
| Windows Ejemplos (nuevo) | Se han agregado nuevos ejemplos al SDK de Windows que muestran el uso de core audio API. Para más información, consulte <a href="sdk-samples-that-use-the-core-audio-apis.md">Ejemplos de SDK que usan las API de audio principales.</a> | 




 

## <a name="major-new-interfaces"></a>Nuevas interfaces principales

Las interfaces siguientes son nuevas para Windows 7:

-   [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)
-   [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)
-   [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)
-   [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)
-   [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)
-   [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)
-   [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)
-   [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)
-   [**IKs JackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)
-   [**IKs JackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows Core Audio API](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




