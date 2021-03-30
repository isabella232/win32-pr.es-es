---
description: Acerca de los códecs de Windows Media
ms.assetid: C0B0265C-AD20-433B-A554-112AEB0208B9
title: Acerca de los códecs de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240176de22682451814609abc94f33a52300563
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279798"
---
# <a name="about-the-windows-media-codecs"></a>Acerca de los códecs de Windows Media

-   [Códecs Windows Media Audio](#windows-media-audio-codecs)
    -   [Windows Media Audio 9](#windows-media-audio-9)
    -   [Windows Media Audio 10 Professional](#windows-media-audio-10-professional)
    -   [Windows Media Audio 9 sin pérdida de](#windows-media-audio-9-lossless)
    -   [Windows Media Audio 9 Voice](#windows-media-audio-9-voice)
    -   [Compatibilidad](#compatibility)
-   [Códecs de la serie Windows Media Video 9](#windows-media-video-9-series-codecs)
    -   [Windows Media Video 9](#windows-media-video-9-series-codecs)
    -   [Pantalla de Windows Media Video 9](#windows-media-video-9-screen)
    -   [Versión 2 de la imagen de Windows Media Video 9](#windows-media-video-9-image-version-2)
    -   [Windows Media Video 9 VCM](#windows-media-video-9-vcm)
    -   [Compatibilidad](#compatibility)
-   [Temas relacionados](#related-topics)

## <a name="windows-media-audio-codecs"></a>Códecs Windows Media Audio

### <a name="windows-media-audio-9"></a>Windows Media Audio 9

Este códec muestrea audio a 44,1 o 48 kilohercios (kHz) con 16 bits, de forma similar al estándar CD actual, que ofrece calidad de CD a velocidades de datos de 64 a 192 kilobits por segundo (kbps). La calidad del sonido resultante es un 20 por ciento mejor que el audio muestreado con Windows Media Audio 8 en las tarifas de datos equivalentes.

El códec Windows Media Audio 9 (WMA 9) admite la codificación de velocidad de bits (VBR) variable, que permite incluso un audio de mayor calidad en tamaños de archivo más pequeños, cambiando automáticamente la velocidad de bits de codificación según la complejidad de los datos de audio. Con VBR, la velocidad de bits de codificación aumenta para capturar secciones complejas de datos y, a continuación, se reduce para maximizar la compresión de las secciones menos complejas, lo que produce una compresión compacta de alta calidad.

WMA 9 es compatible con los descodificadores anteriores compatibles con Windows Media Audio, lo que significa que se puede reproducir contenido de WMA 9 con versiones anteriores de Windows Media Player o dispositivos electrónicos de consumo anteriores que admiten Windows Media. Como con todos los códecs de la serie Windows Media 9, es compatible con la plataforma de administración de derechos digitales de Windows Media, que se usa para empaquetar y distribuir de forma segura los medios digitales protegidos contra copia.

### <a name="windows-media-audio-10-professional"></a>Windows Media Audio 10 Professional

Windows Media Audio 10 Professional (WMA 10 Pro) es el códec de audio de Windows Media más flexible disponible: perfiles de soporte técnico que incluyen todo desde audio de 24 bits/96 kHz en estéreo, canal 5,1 o incluso sonido envolvente de canal 7,1, hasta capacidades móviles altamente eficientes en 24 Kbps hasta 96 kbps para estéreo y 128 Kbps a 256 kbps para sonido de 5,1 Channel. WMA 10 Pro ofrece una calidad increíble para los consumidores que usan Hardware de alta fidelidad y equipos equipados con sonido envolvente de canal 5,1, y para los consumidores que reproducen contenido de audio en sus dispositivos móviles. WMA 10 Pro admite la transmisión por secuencias, la descarga progresiva o la entrega de descarga y reproducción en 128 a 768 kbps.

Cuando se usa audio de sonido envolvente 5,1 comprimido a 384 Kbps con WMA 10 Pro, la mayoría de los agentes de escucha no pueden distinguir las diferencias entre la música comprimida y los archivos de modulación de código de pulso (PCM) originales. WMA Pro también ofrece un control de intervalo dinámico que usa las amplitudes de audio máxima y media que se calculan durante el proceso de codificación. Con la característica modo silencioso de Windows Media Player 9 y versiones posteriores, los usuarios pueden escuchar el intervalo dinámico completo, un intervalo de diferencia media de hasta 12 decibelios (dB) por encima del promedio, o un pequeño intervalo de diferencia de hasta 6 dB por encima del promedio.

Si un usuario intenta reproducir un archivo que se ha codificado mediante el canal 5,1, capacidades de muestreo de 24 bits y 96 kHz, pero no tiene un sistema o tarjeta de sonido que admita sonido de varios canales o de alta resolución, se combinan varios canales en audio estéreo (por ejemplo, de 16 bits, audio de canal de dos), lo que garantiza que los usuarios obtengan la mejor experiencia de reproducción que los sistemas pueden proporcionar.

En la tabla siguiente se compara WMA Pro con la tecnología de compresión de la competencia.



| Datos de audio              | Compresión del sector\*        | Windows Media\*            | Ahorro de compresión |
|-------------------------|-------------------------------|----------------------------|---------------------|
| 2 CH x 48 kHz x 16 bits | Dolby Digital 2,0 a 220 Kbps | WMA 10 Pro a 128 kbps     | 1.7:1               |
| 6 CH x 48 kHz x 20 bits | Dolby Digital 5,1 a 384 Kbps | WMA 10 Pro a 192 – 256 kbps | 1.5 – 2:1             |
| 6 canales x 48 kHz x 24 bits | DTS 5,1 a 1.536 Kbps         | WMA 10 Pro a 768 Kbps     | 2:1                 |



 

\* Dependiente del contenido

### <a name="windows-media-audio-9-lossless"></a>Windows Media Audio 9 sin pérdida de

La calidad de audio del contenido que se comprime con este códec es la mejor de todos los códecs Windows Media Audio. Crea un duplicado de bit por bit del archivo de audio original para que no se pierdan datos, lo que lo hace idóneo para archivar los patrones de contenido.

En función de la complejidad del original, el contenido se comprimirá con una proporción de 2:1 o 3:1. Aunque es menor que la proporción que se logra con otros códecs de la serie Windows Media Audio 9, proporciona las mismas ventajas que la compresión mientras deja los datos intactos.

Como Windows Media Audio 9 Professional, el códec Windows Media Audio 9 Lossless también ofrece un control de intervalo dinámico que usa las amplitudes de audio máxima y media que se calculan durante el proceso de codificación. Con la característica modo silencioso de Windows Media Player 9 y versiones posteriores, los usuarios pueden oír el intervalo dinámico completo, un intervalo de diferencia media de hasta 12 dB por encima del promedio, o un poco de intervalo de diferencia hasta 6 dB por encima del promedio.

### <a name="windows-media-audio-9-voice"></a>Windows Media Audio 9 Voice

Este códec de velocidad de bits bajo está destinado principalmente al contenido de voz, pero funciona muy bien con contenido en modo mixto que incluye voz y música. En el modo de voz, el códec aprovecha la gama de frecuencias relativamente menos complicada y más estrecha de la voz humana para maximizar la compresión. En el modo de música, el códec funciona como el códec estándar de Windows Media Audio 9. El contenido codificado puede configurarse para cambiar entre los modos de voz y música automáticamente.

El códec de voz de Windows Media Audio 9 ofrece una calidad superior para los escenarios de streaming de velocidad de bits baja (menos de 20 Kbps), como difusiones de radio, publicidad, libros electrónicos, podcasts y voces. El códec de voz también puede comprimir el contenido hasta un mínimo de 4 Kbps a 8 kHz.

### <a name="compatibility"></a>Compatibilidad

En la tabla siguiente se describe lo que experimentará su audiencia al reproducir Windows Media Audio contenido de la serie 9 en los sistemas operativos anteriores de Microsoft Windows que Windows XP o con versiones anteriores de Windows Media Player. En esta tabla también se muestra la compatibilidad de las plataformas basadas en Windows CE y Mac OS X de Apple.



| Códec                              | Característica                                       | Compatibilidad con versiones anteriores del reproductor                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Audio 9              | Codificación de velocidad de bits constante (CBR)              | <dl> <dt>Windows Media Player 6,4 o posterior en dispositivos no portátiles (usando transcodificación según sea necesario)</dt> <dt>Windows Media Player 9 para Mac OS X</dt> <dt>Windows Media Player 9 series y Windows Media Player 9,1 para Pocket PC \* </dt> <dt>Windows Media Player series y Windows Media Player 9,1 para smartphone \* </dt> </dl> |
|                                    | Codificación de velocidad de bits variable (VBR)              | Windows Media Player 7 o posterior en todos los dispositivos que admiten el reproductor (usando transcodificación según sea necesario)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Audio 9 Professional | General                                       | <dl> <dt>Windows media Player 7 o posterior</dt> <dt>Windows Media Player 9 para Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Reproducción de canales discretos (por ejemplo, 5,1) | Requiere Windows Media Player 9 Series (o SDK) o posterior, Windows XP y una tarjeta de audio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
|                                    | Audio de alta resolución (24 bits, 96 kHz)        | Requiere Windows Media Player 9 Series (o SDK) o posterior, Windows XP y una tarjeta de audio de alta resolución.                                                                                                                                                                                                                                                                                                                                                                                                                      |
|                                    | Control de intervalo dinámico                         | Requiere Windows Media Player 9 Series (o SDK) o posterior y Windows XP.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Windows Media Audio 9 sin pérdida de     | General                                       | <dl> <dt>Windows media Player 7 o posterior</dt> <dt>Windows Media Player 9 para Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Reproducción de canales discretos (por ejemplo, 5,1) | Requiere Windows Media Player 9 Series (o SDK) o posterior, Windows XP y una tarjeta de audio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Audio 9 Voice        | General                                       | <dl> <dt>Windows Media Player 6,4 o posterior</dt> <dt>Windows Media Player 9 para Mac OS X</dt> <dt>Windows Media Player 9 series y Windows Media Player 9,1 para Pocket PC \* </dt> <dt>Windows Media Player series y Windows Media Player 9,1 para smartphone \* </dt> </dl>                                                       |



 

> [!Note]  
> \* Todas las versiones de Windows Media Player para Pocket PC y smartphone se incluyen como parte del sistema operativo Microsoft Windows Mobile. Windows Media Player para Pocket PC y Windows Media Player para smartphone no están disponibles para su descarga desde Microsoft.

 

## <a name="windows-media-video-9-series-codecs"></a>Códecs de la serie Windows Media Video 9

En 2006, la sociedad de Motion Picture and TV Engineers (SMPTE) publicó formalmente la especificación final de SMPTE 421M, también conocida como VC-1. La normalización formal de VC-1 representa la culminación de años de escrutinio técnico en más de 75 compañías, lo que conduce a un códec que está bien documentado, es sumamente estable y es fácilmente contratable por el sector. VC-1 admite tres perfiles: simple, principal y avanzado. Los perfiles simples y principales se han completado durante varios años, y las implementaciones existentes como WMV 9 han admitido la creación y reproducción de contenido con estos perfiles, así como una implementación temprana del perfil avanzado. La finalización del perfil avanzado y la normalización de todos los perfiles en VC-1 representa el último paso en una especificación completa que ofrece contenido de alta definición (ya sea entrelazado o progresivo) en cualquier medio y en cualquier dispositivo compatible.

### <a name="windows-media-video-9"></a>Windows Media Video 9

Windows Media Video 9 es la implementación de Microsoft del estándar de VC-1 SMPTE. Admite perfiles simples, principales y avanzados.

### <a name="simple-and-main-profiles"></a>Perfiles simples y principales

Los perfiles simples y principales de Windows Media Video 9 se ajustan totalmente al estándar SMPTE VC-1 y proporcionan vídeo de alta calidad para la transmisión por secuencias y la descarga. Estos perfiles admiten una amplia gama de velocidades de bits, desde contenido de alta definición en una mitad a una tercera, la velocidad de bits de MPEG-2 hasta vídeo de Internet de velocidad de bits bajo que se entrega a través de un módem de acceso telefónico. Este códec también admite vídeo descargable de calidad profesional con codificación de dos pasos y de velocidad de bits variable (VBR). Windows Media Video 9 ya es compatible con una amplia variedad de jugadores y dispositivos.

### <a name="advanced-profile"></a>Perfil avanzado

El perfil avanzado de Windows Media Video 9 se ajusta totalmente al estándar SMPTE VC-1, admite contenido entrelazado y es independiente del transporte. Los creadores de contenido pueden usar este perfil para ofrecer contenido progresivo o entrelazado a velocidades de datos tan bajos como un tercio del códec MPEG-2, con la misma calidad que MPEG-2.

En el pasado, el contenido de vídeo entrelazado siempre se desentrelazaba antes de la codificación con el códec de Windows Media Video. Ahora, las aplicaciones de codificación como Windows Media 9 series y las soluciones de codificación de terceros pueden admitir la compresión de contenido entrelazado sin convertirlo primero al contenido progresivo. Es importante mantener el entrelazado en un archivo codificado si el contenido se representa en una pantalla entrelazada, como un televisor.

La independencia de transporte también permite la entrega de un perfil avanzado de Windows Media Video 9 a través de sistemas que no están basados en Windows Media, como las infraestructuras de difusión basadas en estándares (a través de secuencias de transporte MPEG-2 nativas), las infraestructuras inalámbricas (mediante el protocolo de transferencia en tiempo real \[ RTP \] ) o incluso DVDs.

En la tabla siguiente se compara el perfil avanzado de Windows Media Video 9 con la tecnología de compresión de la competencia.



| Datos de vídeo                                                  | Compresión del sector\* | Windows Media\*                                      | Ahorro de compresión |
|-------------------------------------------------------------|------------------------|------------------------------------------------------|---------------------|
| 480/24p 720 x 480 píxeles/fotograma x 8 bits por canal x 24 fps  | MPEG-2 en 4 – 6 Mbps     | Perfil avanzado de Windows Media Video 9 a 1,3 – 2 Mbps | 3:1                 |
| 480/30i 720 x 480 píxeles/fotograma x 8 bits por canal x 30 fps  | MPEG-2 a 6 – 8 Mbps     | Perfil avanzado de Windows Media Video 9 a 2 – 4 Mbps   | 2 – 3:1               |
| 720/24p 1280x720 píxeles/fotograma x 8 bits por canal x 24 fps | MPEG-2 a 19 Mbps      | Perfil avanzado de Windows Media Video 9 a 5 – 8 Mbps   | 2.4 – 3.8:1           |



 

\*Dependiente del contenido

### <a name="windows-media-video-9-screen"></a>Pantalla de Windows Media Video 9

El códec de pantalla de Windows Media Video 9 está optimizado para comprimir capturas de pantalla secuenciales y vídeo muy estático capturado de la pantalla del equipo, lo que lo hace idóneo para entregar demostraciones o para demostrar el uso de equipos para el entrenamiento. El códec aprovecha la simplicidad de imagen típica y la falta de movimiento relativo para lograr una relación de compresión muy alta.

Durante el proceso de codificación, el códec cambia automáticamente entre los modos de codificación perdidos y sin pérdida, en función de la complejidad de los datos de vídeo. En el caso de los datos complejos, el modo sin pérdida conserva una copia exacta de los datos. En el caso de los datos menos complejos, el modo de pérdida descarta algunos datos para lograr una relación de compresión mayor. Al cambiar entre estos dos modos automáticamente, el códec mantiene la calidad del vídeo y maximiza la compresión.

En general, el códec de pantalla de Windows Media Video 9 proporciona un mejor control de las imágenes de mapa de bits y el movimiento de pantalla, incluso en CPU relativamente modestas. También es hasta 100 veces más eficaz que la codificación de longitud de ejecución que se usa con frecuencia.

### <a name="windows-media-video-9-image-version-2"></a>Versión 2 de la imagen de Windows Media Video 9

El códec de imagen 2 de Windows Media Video 9 es diferente del resto de códecs de vídeo. En lugar de procesar vídeo sin comprimir, transforma imágenes fijas en vídeo mediante el uso de pan, zoom y transiciones transversales entre clips para crear un número ilimitado de efectos.

Los resultados se pueden entregar a la velocidad de datos de hasta 20 kilobits por segundo (kbps). Estos archivos se comprimen con la velocidad de bits constante (CBR) o con los modos de velocidad de bits variable (VBR) de un paso.

> [!Note]  
> El códec de imagen 2 de Windows Media Video 9 no es compatible con el códec de imagen de Windows Media Video 9.

 

### <a name="windows-media-video-9-vcm"></a>Windows Media Video 9 VCM

La versión del administrador de compresión de vídeo (VCM) del códec de la serie Windows Media Video 9 permite que las versiones anteriores de las aplicaciones de codificación y edición admitan el códec de la serie Windows Media Video 9 en contenedores de archivos como audio y vídeo intercalado (AVI). Este paquete de códecs también permite reproducir archivos Windows Media Video (WMV) basados en Windows Media Format 9 series en Windows Media Player 6,4, en contenedores de archivos ASF y AVI.

### <a name="compatibility"></a>Compatibilidad

En la tabla siguiente se describe lo que experimentará su audiencia al reproducir Windows Media Video contenido de la serie 9 en los sistemas operativos anteriores de Microsoft Windows o en versiones anteriores de Windows Media Player. En esta tabla también se muestra la compatibilidad de las plataformas basadas en Windows CE y Mac OS X de Apple.



| Códec                                  | Característica             | Compatibilidad con versiones anteriores del reproductor                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 9                  | General             | <dl> <dt>Windows Media Player 6,4 o posterior</dt> <dt>Windows Media Player 9 para Mac OS X</dt> <dt>Windows Media Player 9 series y Windows Media Player 9,1 para Pocket PC \* </dt> <dt>Windows Media Player series y Windows Media Player 9,1 para smartphone \* </dt> </dl> |
|                                        | Interpolación de fotogramas | Requiere Windows Media Player 9 Series (o kit de desarrollo de software) o posterior y Windows XP.                                                                                                                                                                                                                                                                                                                                                                           |
| Perfil avanzado de Windows Media Video 9 | General             | Windows Media Player 7 o posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Pantalla de Windows Media Video 9           | General             | Windows Media Player 7 o posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Versión 2 de la imagen de Windows Media Video 9  | General             | Windows Media Player 7 o posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

> [!Note]  
> \*Todas las versiones de Windows Media Player para Pocket PC y smartphone se incluyen como parte del sistema operativo Microsoft Windows Mobile. Windows Media Player para Pocket PC y Windows Media Player para smartphone no están disponibles para su descarga desde Microsoft.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



