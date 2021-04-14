---
title: Plataforma multimedia
description: Media Foundation y DirectShow proporcionan la base para la compatibilidad con medios en Windows.
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f756112384451ac3f5b4055d73a60a170b2e29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533442"
---
# <a name="media-platform"></a>Plataforma multimedia

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) y [DirectShow](/windows/desktop/DirectShow/directshow) proporcionan la base para la compatibilidad con medios en Windows. Media Foundation se presentó en Windows Vista como sustituto de DirectShow. En Windows 7, Media Foundation se ha mejorado para proporcionar una mejor compatibilidad con el formato, incluido *MPEG-4*, así como compatibilidad con dispositivos de captura de vídeo y códecs de hardware.

## <a name="format-support"></a>Compatibilidad con formato

En Windows 7, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) proporciona una compatibilidad de formato amplia que incluye códecs para vídeo *H. 264* , *MJPEG* y *mp3*. nuevos orígenes para *MP4*, *3GP*, audio *AAC* y *AVI*; y nuevos receptores de archivo para *MP4*, *3GP* y *mp3*. (Consulte [formatos de medios compatibles en Media Foundation](../medfound/supported-media-formats-in-media-foundation.md)).

## <a name="hardware-devices"></a>Dispositivos de hardware

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) ahora admite los siguientes tipos de dispositivos de hardware en la canalización de audio y vídeo:

-   Dispositivos de captura de vídeo de *UVC 1,1* , como cámaras Web
-   Dispositivos de captura de audio
-   Codificadores y descodificadores de hardware
-   Procesadores de vídeo de hardware, como convertidores de espacio de color

Los códecs de hardware pueden realizar una transcodificación de vídeo muy rápida. Por ejemplo, supongamos que desea transferir un archivo *Windows Media Video (WMV)* a un teléfono móvil que solo admita archivos *3GP* . Con un codificador de hardware, el archivo se puede transcodificar "según sea necesario" inmediatamente antes de transferirlo al dispositivo.

Los dispositivos de hardware se representan en [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) mediante un objeto proxy, y se usan en la canalización como componentes basados en software. (Vea las novedades [de Media Foundation](../medfound/whats-new-for-media-foundation.md)).

## <a name="simplified-programming-model"></a>Modelo de programación simplificado

En Windows Vista, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) expone un conjunto de API de nivel relativamente bajo. Estas API son flexibles, pero puede que no sean adecuadas para realizar tareas. Windows 7 agrega nuevas API de alto nivel que facilitan la escritura de aplicaciones multimedia en *C++*. Estas nuevas API de alto nivel incluyen:

-   **MFPlay**. Estas API están diseñadas para la reproducción de audio y vídeo. Admiten las operaciones de reproducción típicas (detener, pausar, reproducir, buscar, control de velocidad, volumen de audio, etc.) y ocultar los detalles de las API de bajo nivel (la sesión y las capas de la topología).
-   **Lector de origen**. Puede usar estas API para extraer datos sin procesar o descodificar de un archivo multimedia, sin conocer nada sobre el formato subyacente. Por ejemplo, puede obtener un mapa de bits en miniatura de un archivo de vídeo u obtener fotogramas de vídeo en directo desde una cámara web.
-   **Escritor de receptor**. Puede usar estas API para crear archivos multimedia pasando datos sin comprimir o codificados. Por ejemplo, puede volver a codificar o Remix un archivo de vídeo.
-   **Transcode**. Estas API se dirigen a los escenarios de codificación de audio y vídeo más comunes.

## <a name="platform-improvements"></a>Mejoras en la plataforma

Windows 7 incluye numerosas mejoras en las API de la plataforma de [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) subyacente. Las aplicaciones avanzadas pueden usar estas API directamente; otras aplicaciones obtendrán las ventajas indirectamente. Entre las ventajas se incluye lo siguiente:

-   Mejoras en la canalización de vídeo para reducir el consumo de energía y el uso de memoria de vídeo.
-   Nuevas API de procesamiento de vídeo *DVXA* , que usan un modelo de composición más flexible y son más adecuados para los formatos de vídeo *HD* .
-   Mejoras en la forma en que se enumeran y administran los complementos (orígenes y descodificadores).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Media Foundation](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 