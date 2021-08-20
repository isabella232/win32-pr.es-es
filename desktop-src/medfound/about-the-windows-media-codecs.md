---
description: Acerca de los códecs Windows multimedia
ms.assetid: C0B0265C-AD20-433B-A554-112AEB0208B9
title: Acerca de los códecs Windows multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 319f7ab16eea462233df994f32b3e3128997f1074e3c7ff69df9885b437f2783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065495"
---
# <a name="about-the-windows-media-codecs"></a>Acerca de los códecs Windows multimedia

-   [Windows Códecs de audio multimedia](#windows-media-audio-codecs)
    -   [Windows Audio multimedia 9](#windows-media-audio-9)
    -   [Windows Audio multimedia 10 Professional](#windows-media-audio-10-professional)
    -   [Windows Audio multimedia 9 sin pérdida](#windows-media-audio-9-lossless)
    -   [Windows Media Audio 9 Voice](#windows-media-audio-9-voice)
    -   [Compatibilidad](#compatibility)
-   [Windows Códecs de la serie Media Video 9](#windows-media-video-9-series-codecs)
    -   [Windows Vídeo multimedia 9](#windows-media-video-9-series-codecs)
    -   [Windows Pantalla vídeo multimedia 9](#windows-media-video-9-screen)
    -   [Windows Imagen de Media Video 9 versión 2](#windows-media-video-9-image-version-2)
    -   [Windows Vídeo multimedia 9 VCM](#windows-media-video-9-vcm)
    -   [Compatibilidad](#compatibility)
-   [Temas relacionados](#related-topics)

## <a name="windows-media-audio-codecs"></a>Windows Códecs de audio multimedia

### <a name="windows-media-audio-9"></a>Windows Audio multimedia 9

Este códec muestrea audio a 44,1 o 48 kilohercios (kHz) con 16 bits, similar al estándar de CD actual, que ofrece una calidad de CD a velocidades de datos de 64 a 192 kilobits por segundo (Kbps). La calidad de sonido resultante es un 20 % mejor que el audio muestreado con Windows Media Audio 8 a velocidades de datos equivalentes.

El códec Windows Media Audio 9 (WMA 9) admite la codificación de velocidad de bits variable (VBR), que permite audio de mayor calidad en tamaños de archivo más pequeños al variar automáticamente la velocidad de bits de codificación según la complejidad de los datos de audio. Con VBR, la velocidad de bits de codificación aumenta para capturar secciones complejas de datos y, a continuación, disminuye para maximizar la compresión de las secciones menos complejas, generando compresión compacta y de alta calidad.

WMA 9 es compatible con versiones anteriores con descodificadores compatibles con Windows Media Audio, lo que significa que el contenido de WMA 9 se puede reproducir con versiones anteriores de Reproductor de Windows Media o dispositivos electrónicos de consumidor anteriores que admiten Windows Media. Al igual que con todos Windows códecs de la serie Media 9, admite la plataforma de administración de derechos digitales de Windows Media, que se usa para empaquetar y distribuir de forma segura medios digitales protegidos con copia.

### <a name="windows-media-audio-10-professional"></a>Windows Audio multimedia 10 Professional

Windows Media Audio 10 Professional (WMA 10 Pro) es el códec de audio multimedia de Windows más flexible disponible, que admite perfiles que incluyen todo, desde audio de 24 bits/96 kHz de resolución completa en estéreo, Canal 5.1, o incluso sonido envolvente de canal 7.1, a funcionalidades móviles altamente eficientes de 24 Kbps a 96 Kbps para estéreo y de 128 Kbps a 256 Kbps para sonido de 5.1 canales. WMA 10 Pro ofrece una calidad increíble para los consumidores que usan hardware de alta fidelidad y un canal 5.1 que rodean equipos equipados con sonido, y para los consumidores que reproducen contenido de audio en sus dispositivos móviles. El Pro WMA 10 admite streaming, descarga progresiva o entrega de descarga y reproducción de 128 a 768 Kbps.

Cuando se usa el audio de sonido envolvente 5.1 comprimido a 384 Kbps con WMA 10 Pro, la mayoría de los agentes de escucha no pueden distinguir las diferencias entre la música comprimida y los archivos originales de compresión de código de pulso (PCM). WMA Pro también ofrece control de intervalo dinámico mediante las amplitudes de audio máximas y medias que se calculan durante el proceso de codificación. Con la característica Modo silencioso de Reproductor de Windows Media 9 y versiones posteriores, los usuarios pueden escuchar el intervalo dinámico completo, un intervalo de diferencia medio de hasta 12 decibelos (dB) por encima del promedio o un intervalo de diferencias de hasta 6 dB por encima del promedio.

Si un usuario intenta reproducir un archivo codificado mediante el canal 5.1, capacidades de muestreo de 24 bits y 96 kHz, pero no tiene un sistema o una tarjeta de sonido que admita sonido multicanal o de alta resolución, varios canales se combinan en audio estéreo (por ejemplo, audio de 16 bits y dos canales), lo que garantiza que los usuarios obtengan la mejor experiencia de reproducción que sus sistemas pueden proporcionar.

En la tabla siguiente se comparan los Pro WMA con la tecnología de compresión de la competencia.



| Datos de audio              | Compresión del sector\*        | Windows Medio\*            | Ahorro de compresión |
|-------------------------|-------------------------------|----------------------------|---------------------|
| 2 ch x 48 kHz x 16 bits | Dolby Digital 2.0 a 220 Kbps | WMA 10 Pro a 128 Kbps     | 1.7:1               |
| 6 ch x 48 kHz x 20 bits | Dolby Digital 5.1 a 384 Kbps | WMA 10 Pro a 192-256 Kbps | 1.5–2:1             |
| 6 ch x 48 kHz x 24 bits | DTS 5.1 a 1536 Kbps         | WMA 10 Pro a 768 Kbps     | 2:1                 |



 

\* Dependiente del contenido

### <a name="windows-media-audio-9-lossless"></a>Windows Audio multimedia 9 sin pérdida

La calidad de audio del contenido que se comprime con este códec es la mejor de todas Windows códecs de audio multimedia. Crea un duplicado bit a bit del archivo de audio original para que no se pierdan datos, lo que lo hace ideal para archivar los maestros de contenido.

Según la complejidad del original, el contenido se comprimirá con una relación de 2:1 o 3:1. Aunque es inferior a la relación lograda con otros códecs de la serie Windows Media Audio 9, proporciona las mismas ventajas de compresión y, al mismo tiempo, deja intactos los datos.

Al Windows Media Audio 9 Professional, el códec sin pérdida de Windows Media Audio 9 también ofrece control de intervalo dinámico mediante las amplitudes de audio máximas y medias que se calculan durante el proceso de codificación. Con la característica Modo silencioso de Reproductor de Windows Media 9 y versiones posteriores, los usuarios pueden escuchar el intervalo dinámico completo, un intervalo de diferencia medio de hasta 12 dB por encima del promedio o un intervalo de diferencias de hasta 6 dB por encima de la media.

### <a name="windows-media-audio-9-voice"></a>Windows Media Audio 9 Voice

Este códec de baja velocidad de bits está destinado principalmente al contenido de voz, pero funciona muy bien con contenido en modo mixto que incluye voz y música. En el modo de voz, el códec aprovecha el intervalo de frecuencia relativamente menos complicado y más estrecho de la voz humana para maximizar la compresión. En el modo de música, el códec funciona como el códec Windows Media Audio 9. El contenido codificado se puede configurar para cambiar automáticamente entre los modos de voz y música.

El códec de voz Windows Media Audio 9 ofrece una calidad superior para escenarios de streaming de baja velocidad de bits (menos de 20 Kbps), como difusión de radio, publicidad, libros electrónicos, podcasts y voiceovers. El códec de voz también puede comprimir el contenido a tan solo 4 Kbps a 8 kHz.

### <a name="compatibility"></a>Compatibilidad

En la tabla siguiente se describe lo que experimentará la audiencia al reproducir contenido de la serie Media Audio 9 de Windows en sistemas operativos anteriores de Microsoft Windows que Windows XP o con versiones anteriores de Reproductor de Windows Media. En esta tabla también se muestra la compatibilidad de apple Mac OS X plataformas Windows CE basadas en aplicaciones.



| Códec                              | Característica                                       | Compatibilidad con versiones anteriores del reproductor                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Audio multimedia 9              | Codificación de velocidad de bits constante (CBR)              | <dl> <dt>Reproductor de Windows Media 6.4</dt> o posterior en dispositivos no portátiles (mediante transcodificación según sea necesario) Reproductor de Windows Media <dt>9</dt> para Mac OS X Reproductor de Windows Media serie 9 y <dt>Reproductor de Windows Media \* 9.1</dt> para la serie Pocket PC Reproductor de Windows Media 9 y <dt>Reproductor de Windows Media \* 9.1</dt> para smartphone </dl> |
|                                    | Codificación de velocidad de bits variable (VBR)              | Reproductor de Windows Media 7 o posterior en todos los dispositivos que admiten el reproductor (mediante la transcodificación según sea necesario)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Audio multimedia 9 Professional | General                                       | <dl> <dt>Reproductor de Windows Media 7 o posterior</dt> <dt>Reproductor de Windows Media 9 para Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Reproducción discreta del canal (por ejemplo, 5.1) | Requiere Reproductor de Windows Media serie 9 (o SDK) o posterior, Windows XP y una tarjeta de audio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
|                                    | Audio de alta resolución (24 bits, 96 kHz)        | Requiere Reproductor de Windows Media serie 9 (o SDK) o posterior, Windows XP y una tarjeta de audio de alta resolución.                                                                                                                                                                                                                                                                                                                                                                                                                      |
|                                    | Control de intervalo dinámico                         | Requiere Reproductor de Windows Media serie 9 (o SDK) o posterior y Windows XP.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Windows Audio multimedia 9 sin pérdida     | General                                       | <dl> <dt>Reproductor de Windows Media 7 o posterior</dt> <dt>Reproductor de Windows Media 9 para Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Reproducción discreta del canal (por ejemplo, 5.1) | Requiere Reproductor de Windows Media serie 9 (o SDK) o posterior, Windows XP y una tarjeta de audio multicanal.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Audio 9 Voice        | General                                       | <dl> <dt>Reproductor de Windows Media 6.4</dt> o posterior <dt>Reproductor de Windows Media 9</dt> para Mac OS X Reproductor de Windows Media serie 9 y <dt>Reproductor de Windows Media 9.1 \* </dt> para Pocket PC Reproductor de Windows Media serie 9 y <dt>Reproductor de Windows Media 9.1 para smartphone \* </dt> </dl>                                                       |



 

> [!Note]  
> \*Todas las versiones de Reproductor de Windows Media para Pocket PC y Smartphone se envían como parte del sistema operativo Microsoft Windows Mobile. Reproductor de Windows Media para Pocket PC y Reproductor de Windows Media para Smartphone no están disponibles para su descarga desde Microsoft.

 

## <a name="windows-media-video-9-series-codecs"></a>Windows Códecs de la serie Media Video 9

En 2006, la Society of Motion Picture and Tv Engineers (SMPTE) publicó formalmente la especificación final para SMPTE 421M, también conocida como VC-1. La normalización formal de VC-1 representa la vocación de años de examen técnico por parte de más de 75 empresas, lo que conduce a un códec bien documentado, extremadamente estable, fácilmente licensable y aceptado por el sector. VC-1 admite tres perfiles: Simple, Main y Advanced. Los perfiles Simple y Main se han completado durante varios años y las implementaciones existentes, como WMV 9, han admitido durante mucho tiempo la creación y reproducción de contenido mediante estos perfiles, así como una implementación temprana del perfil Avanzado. La finalización del perfil avanzado y la consiguiente normalización de todos los perfiles en VC-1 representa el paso final de una especificación completa que proporciona contenido de alta definición, entrelazado o progresiva, en cualquier dispositivo medio y compatible.

### <a name="windows-media-video-9"></a>Windows Vídeo multimedia 9

Windows Media Video 9 es la implementación de Microsoft del estándar VC-1 SMPTE. Admite perfiles simples, principales y avanzados.

### <a name="simple-and-main-profiles"></a>Perfiles simples y principales

Los perfiles Windows Media Video 9 Simple y Main se ajustan totalmente al estándar SMPTE VC-1 y proporcionan vídeo de alta calidad para streaming y descarga. Estos perfiles admiten una amplia gama de velocidades de bits, desde contenido de alta definición a la mitad a un tercio de la velocidad de bits de MPEG-2, hasta vídeo de Internet de baja velocidad de bits entregado a través de un módem de acceso telefónico. Este códec también admite vídeo descargable de calidad profesional con codificación de velocidad de bits variable (VBR) y de dos pases. Windows Media Video 9 ya es compatible con una amplia variedad de reproductores y dispositivos.

### <a name="advanced-profile"></a>Perfil avanzado

El perfil Windows Media Video 9 Advanced se ajusta totalmente al estándar SMPTE VC-1, admite contenido entrelazado y es independiente del transporte. Los creadores de contenido pueden usar este perfil para ofrecer contenido progresiva o entrelazado a velocidades de datos tan baja como un tercio de la del códec MPEG-2, con la misma calidad que MPEG-2.

En el pasado, el contenido de vídeo entrelazado siempre se desenlazaba antes de codificar con el códec Windows media video. Ahora, las aplicaciones de codificación como Windows Media 9 Series y las soluciones de codificación de terceros pueden admitir la compresión de contenido entrelazado sin convertirlo primero en contenido progresiva. Mantener el entrelazado en un archivo codificado es importante si el contenido se representa alguna vez en una pantalla entrelazada, como un televisor.

La independencia del transporte también permite la entrega del perfil avanzado de Windows Media Video 9 a través de sistemas que no están basados en medios de Windows, como infraestructuras de difusión basadas en estándares (a través de secuencias de transporte MPEG-2 nativas), infraestructuras inalámbricas (mediante el protocolo de transferencia en tiempo real RTP) o incluso \[ \] DVD.

En la tabla siguiente se compara Windows perfil avanzado de Media Video 9 con la tecnología de compresión de la competencia.



| Datos de vídeo                                                  | Compresión del sector\* | Windows Medio\*                                      | Ahorro de compresión |
|-------------------------------------------------------------|------------------------|------------------------------------------------------|---------------------|
| 480/24p 720x480 píxeles/fotograma x 8 bits por canal x 24 fps  | MPEG-2 a 4-6 Mbps     | Windows Perfil avanzado de Media Video 9 a 1,3-2 Mbps | 3:1                 |
| 480/30i 720 x 480 píxeles/fotograma x 8 bits por canal x 30 fps  | MPEG-2 a 6-8 Mbps     | Windows Perfil avanzado de Media Video 9 a 2-4 Mbps   | 2–3:1               |
| 720/24p 1280 x 720 píxeles/fotograma x 8 bits por canal x 24 fps | MPEG-2 a 19 Mbps      | Windows Perfil avanzado de Media Video 9 a 5-8 Mbps   | 2.4–3.8:1           |



 

\*Dependiente del contenido

### <a name="windows-media-video-9-screen"></a>Windows Pantalla vídeo multimedia 9

El códec de pantalla Windows Media Video 9 está optimizado para comprimir capturas de pantalla secuenciales y vídeo altamente estático que se captura de la pantalla del equipo, lo que lo hace ideal para entregar demostraciones o demostrar el uso del equipo para el entrenamiento. El códec aprovecha la simplicidad típica de la imagen y la falta relativa de movimiento para lograr una relación de compresión muy alta.

Durante el proceso de codificación, el códec cambia automáticamente entre los modos de codificación sin pérdida y pérdida de datos, en función de la complejidad de los datos de vídeo. En el caso de los datos complejos, el modo sin pérdida conserva una copia exacta de los datos. En el caso de los datos menos complejos, el modo de pérdida descarta algunos datos para lograr una mayor relación de compresión. Al cambiar automáticamente entre estos dos modos, el códec mantiene la calidad del vídeo al tiempo que maximiza la compresión.

En general, el códec Windows Media Video 9 Screen ofrece un mejor control de las imágenes de mapa de bits y el movimiento de la pantalla, incluso en CPU relativamente moderadas. También es hasta 100 veces más eficaz que la codificación de longitud de ejecución usada habitualmente.

### <a name="windows-media-video-9-image-version-2"></a>Windows Imagen de Media Video 9 versión 2

El Windows de imagen 2 de Media Video 9 es diferente del resto de códecs de vídeo. En lugar de procesar vídeo sin comprimir, transforma imágenes fijas en vídeo mediante transiciones de desplazamiento panorámico, zoom y atenuación cruzada entre clips para crear un número ilimitado de efectos.

Los resultados se pueden entregar a velocidades de datos de tan solo 20 kilobits por segundo (Kbps). Estos archivos se comprimen mediante los modos de velocidad de bits constante (CBR) o velocidad de bits variable de un paso (VBR).

> [!Note]  
> El Windows de imagen 2 de Media Video 9 no es compatible con el códec Windows imagen de Media Video 9.

 

### <a name="windows-media-video-9-vcm"></a>Windows Vídeo multimedia 9 VCM

La versión del Administrador de compresión de vídeo (VCM) del códec de la serie Windows Media Video 9 permite que las versiones anteriores de las aplicaciones de codificación y edición admitan el códec de la serie Windows Media Video 9 en contenedores de archivos como Audio Video Interleaved (AVI). Este paquete de códec también permite Windows Archivos de vídeo multimedia (WMV) basados en la serie formato multimedia 9 de Windows que se reproducen en Reproductor de Windows Media 6.4, en contenedores de archivos ASF y AVI.

### <a name="compatibility"></a>Compatibilidad

En la tabla siguiente se describe lo que experimentará la audiencia al reproducir contenido de la serie Windows Media Video 9 en sistemas operativos anteriores de Microsoft Windows o con versiones anteriores de Reproductor de Windows Media. En esta tabla también se muestra la compatibilidad de apple Mac OS X plataformas Windows CE basadas en aplicaciones.



| Códec                                  | Característica             | Compatibilidad con versiones anteriores del reproductor                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vídeo multimedia 9                  | General             | <dl> <dt>Reproductor de Windows Media 6.4</dt> o posterior <dt>Reproductor de Windows Media 9</dt> para Mac OS X Reproductor de Windows Media serie 9 y <dt>Reproductor de Windows Media 9.1 \* </dt> para Pocket PC Reproductor de Windows Media serie 9 y <dt>Reproductor de Windows Media 9.1 para smartphone \* </dt> </dl> |
|                                        | Interpolación de fotogramas | Requiere Reproductor de Windows Media serie 9 (o Kit de desarrollo de software) o posterior y Windows XP.                                                                                                                                                                                                                                                                                                                                                                           |
| Windows Perfil avanzado de Media Video 9 | General             | Reproductor de Windows Media 7 o posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Pantalla vídeo multimedia 9           | General             | Reproductor de Windows Media 7 o posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Imagen de Media Video 9 versión 2  | General             | Reproductor de Windows Media 7 o posterior                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

> [!Note]  
> \*Todas las versiones de Reproductor de Windows Media para Pocket PC y Smartphone se envían como parte del sistema operativo Microsoft Windows Mobile. Reproductor de Windows Media para Pocket PC y Reproductor de Windows Media para Smartphone no están disponibles para su descarga desde Microsoft.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



