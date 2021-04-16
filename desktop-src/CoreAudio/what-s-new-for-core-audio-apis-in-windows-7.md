---
description: Las API de audio principales se introdujeron en Windows Vista, que ofrecía un nuevo conjunto de componentes de audio de modo de usuario que una aplicación cliente puede usar para representar o capturar secuencias de audio con capacidades de audio mejoradas.
ms.assetid: eb99c266-16d2-4a14-bc1d-059a0a94db13
title: Novedades de las API de audio principales en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c87a4daa9e645587253239082475e59fd1563c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659556"
---
# <a name="whats-new-for-core-audio-apis-in-windows-7"></a>Novedades de las API de audio principales en Windows 7

Las API de audio principales se introdujeron en Windows Vista, que ofrecía un nuevo conjunto de componentes de audio de modo de usuario que una aplicación cliente puede usar para representar o capturar secuencias de audio con capacidades de audio mejoradas. Para obtener información general sobre este conjunto de API, consulte [acerca de las API de audio de Windows Core](about-the-windows-core-audio-apis.md).

Las API de audio principales se han mejorado en Windows 7. En la tabla siguiente se resumen las nuevas características y las mejoras de las API de audio principales:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Característica</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mejoras genéricas</td>
<td>Las siguientes características se han mejorado en Windows 7:
<ul>
<li>En el modo de uso compartido de Windows 7, los flujos se ejecutan en <em>modo de latencia baja</em>. El motor de audio se ejecuta en modo de extracción con una reducción significativa de la latencia. Esto es muy útil para las aplicaciones de comunicación que requieren una baja latencia de secuencia de audio para una transmisión por secuencias más rápida.</li>
<li>Windows 7 proporciona una mejor detección de roles de dispositivo cuando se agrega un nuevo dispositivo al sistema. Para obtener más información, consulte <a href="device-roles-in-windows-vista.md">trabajar con roles de dispositivo</a>.</li>
<li>En Windows 7, puede escuchar música desde el reproductor multimedia portátil a través de los altavoces del equipo. Puede usar esta característica del monitor de captura conectando un reproductor multimedia portátil al equipo con un cable de audio analógico. En el pasado, algunos OEM han proporcionado esta funcionalidad en el controlador de audio mediante un bucle invertido de hardware. En Windows 7, esta funcionalidad se ha agregado al sistema operativo. Dado que se encuentra en el sistema y no en el controlador, puede utilizarlo para cualquier otro dispositivo conectado al sistema, como un casco USB.</li>
<li>El audio HDMI se ha mejorado en Windows 7, que proporciona compatibilidad con el formato de velocidad de bits alto. Con esta mejora, puede admitir audio multicanal y formatos de audio comprimidos a través de un conector HDMI para un receptor de audio.</li>
<li>En Windows Vista, Windows Media Player reproduce música solo a través del dispositivo de audio predeterminado, que el usuario no puede cambiar. Para que Windows Media Player represente audio en un dispositivo determinado, el dispositivo predeterminado debe cambiarse en el panel de control <strong>sonido</strong> . En Windows 7, Windows Media Player proporciona las API que permiten que una aplicación se represente en cualquier dispositivo seleccionado por el usuario, no solo el dispositivo predeterminado.</li>
<li>En Windows Vista, si un equipo que está reproduciendo audio cambia al modo de ahorro de energía, el equipo está bloqueado y, si el usuario desea interrumpir la reproducción, el usuario debe iniciar sesión y presionar la tecla detener para detener la reproducción. En Windows 7, si el equipo está bloqueado, todavía puede controlar la reproducción mediante el control HID del teclado.</li>
<li>Windows 7 reduce el consumo de energía de cualquier aplicación que use DirectSound y DirectShow para representar los medios. Además, el servicio Programador de clases multimedia habilita el audio resistente a problemas y utiliza menos energía mientras se generan los ejemplos de audio.</li>
</ul></td>
</tr>
<tr class="even">
<td>Dispositivo de comunicación (nuevo)</td>
<td>En esta versión, se ha agregado un nuevo tipo de dispositivo al panel de control <strong>sonidos</strong> : dispositivo de <strong>comunicaciones</strong> . Este dispositivo se usa principalmente para las comunicaciones, es decir, para colocar o recibir llamadas telefónicas en el equipo. Una aplicación de comunicación puede usar los componentes de audio principales para obtener una referencia al punto de conexión del dispositivo de comunicación predeterminado y representar secuencias de audio para fines de comunicación. El sistema operativo considera que el flujo abierto en un dispositivo de comunicación es un flujo de comunicación. Las operaciones de WASAPI en un flujo de comunicación son similares a cualquier otra secuencia de audio. Para obtener más información, consulte <a href="device-roles-in-windows-vista.md">trabajar con roles de dispositivo</a>.</td>
</tr>
<tr class="odd">
<td>Atenuación de la secuencia o pato de audio (nuevo)</td>
<td>La nueva característica de Windows 7, que se ha diseñado para las aplicaciones de comunicación unificada y VoIP <a href="stream-attenuation.md">, es una</a> nueva característica de Windows 7. De forma predeterminada, el sistema operativo reduce la intensidad de una secuencia de audio cuando se recibe un flujo de comunicación, como una llamada de teléfono, en el dispositivo de comunicación a través del equipo. El usuario establece las opciones de volumen en el panel de control de <strong>sonido</strong> . Se han agregado nuevas API en el Windows SDK que permiten a las aplicaciones reemplazar el comportamiento predeterminado de los patos. Para obtener más información sobre la implementación de una característica de patos personalizada, vea <a href="providing-a-custom-ducking-experience.md">proporcionar un comportamiento personalizado de pato</a>. <br/></td>
</tr>
<tr class="even">
<td>Enrutamiento de flujo (nuevo)</td>
<td>En Windows 7, las API de audio principales se han mejorado para transferir una transmisión de audio sin problemas desde un dispositivo existente a un nuevo punto de conexión de audio predeterminado. Los conjuntos de API de audio de alto nivel que usan las API de audio principales, como Media Foundation, DirectSound y las API de WAVE, implementan la característica de enrutamiento de flujo. Las aplicaciones multimedia que usan estos conjuntos de API para reproducir o capturar un flujo usan la implementación predeterminada y no tienen que modificar la aplicación. Sin embargo, si la aplicación multimedia usa directamente las API de audio principales, la aplicación debe proporcionar la implementación de enrutamiento de flujo. Para ello, la aplicación debe controlar los nuevos eventos que se han agregado que notifican a un cliente de WASAPI cuando el dispositivo predeterminado está conectado o quitado. Para obtener más información sobre esta característica, consulte <a href="stream-routing.md">enrutamiento de flujo</a>.</td>
</tr>
<tr class="odd">
<td>Audio de modo de usuario protegido (PUMA) (mejorado)</td>
<td>PUMA se ha actualizado para Windows 7 con el fin de proporcionar las siguientes características:
<ul>
<li>Establecer bits del sistema de administración de copia en serie (SCMS) en puntos de conexión S/PDIF y bits de Content Protection digital (HDCP) de ancho de banda alto en los puntos de conexión de la interfaz multimedia High-Definition (HDMI).</li>
<li>Habilitación de los controles de protección SCMS y HDMI fuera de un entorno protegido (PE).</li>
</ul>
Para obtener más información acerca de las mejoras, consulte <a href="protected-user-mode-audio--puma-.md">audio de modo de usuario protegido (Puma)</a>.<br/></td>
</tr>
<tr class="even">
<td>La estructura <strong>WAVEFORMATEXTENSIBLE</strong> se ha extendido a la estructura <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> (nueva)</td>
<td>En Windows 7, se ha agregado una nueva estructura para admitir transmisiones IEC 61937. <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> extiende la estructura <strong>WAVEFORMATEXTENSIBLE</strong> para almacenar dos conjuntos de características de secuencia de audio: el formato de audio codificado antes de la transmisión y las características de la secuencia de audio después de que se haya descodificado. La nueva estructura especifica explícitamente el número efectivo de canales, el tamaño de la muestra y la velocidad de datos de un formato no PCM. Con esta información, una aplicación puede inferir el nivel de calidad de la secuencia que no es PCM una vez descomprimido y reproducido. Para obtener más información, vea <a href="representing-formats-for-iec-61937-transmissions.md">representating Formats for IEC 61937 transmisiones</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient:: Initialize</strong></a> (mejorado)</td>
<td>El método <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient:: Initialize</strong></a> se ha mejorado para indicar errores específicos que pueden producirse al abrir una secuencia de audio. Los nuevos códigos de error son:
<ul>
<li>AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED</li>
<li>AUDCLNT_E_BUFFER_SIZE_ERROR</li>
<li>AUDCLNT_E_INVALID_DEVICE_PERIOD</li>
</ul>
Para obtener más información sobre estos errores, vea la sección valor devuelto en <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient:: Initialize</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient:: getBuffer</strong></a> y <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient:: getBuffer</strong></a> (mejorado)</td>
<td>Los métodos <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient:: getBuffer</strong></a> y <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient:: getBuffer</strong></a> se han mejorado para devolver el AUDCLNT_E_BUFFER_ERROR código de error que indica que no se recuperó el búfer del extremo en el modo exclusivo. Para obtener más información, vea comentarios en <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient:: getBuffer</strong></a> y <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient:: getBuffer</strong></a>.</td>
</tr>
<tr class="odd">
<td>Funcionalidad de detección de conectores (mejorada)</td>
<td>Una nueva interfaz en Windows 7, <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2"><strong>IKsJackDescription2</strong></a>, extiende <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription"><strong>IKsJackDescription</strong></a>. Mediante el uso de la nueva interfaz, la pila de audio o una aplicación pueden obtener información adicional sobre los conectores. Esto incluye la capacidad de detección del conector y si el formato del dispositivo ha cambiado dinámicamente.</td>
</tr>
<tr class="even">
<td>Ejemplos de Windows (nuevo)</td>
<td>Se han agregado nuevos ejemplos a la Windows SDK que muestran el uso de las API de audio principales. Para obtener más información, consulte <a href="sdk-samples-that-use-the-core-audio-apis.md">ejemplos de SDK que usan las API de audio principales</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="major-new-interfaces"></a>Nuevas interfaces principales

Las siguientes interfaces son nuevas para Windows 7:

-   [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)
-   [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)
-   [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)
-   [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)
-   [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)
-   [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)
-   [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)
-   [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)
-   [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)
-   [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las API de audio de Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




