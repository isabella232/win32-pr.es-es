---
title: Plataforma multimedia
description: Media Foundation y DirectShow proporcionan la base para la compatibilidad con medios en Windows.
ms.assetid: 020f009c-7432-432b-a39b-9295dd784d2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a4db7d84745f64f3fe80faed267e58d1f5ddbce4ab82ed75b38453f82b0e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964584"
---
# <a name="media-platform"></a>Plataforma multimedia

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) [y](/windows/desktop/DirectShow/directshow) DirectShow proporcionan la base para la compatibilidad con medios en Windows. Media Foundation se introdujo en Windows Vista como reemplazo de DirectShow. En Windows 7, Media Foundation se ha mejorado para proporcionar una mejor compatibilidad con el formato, incluido *MPEG-4,* así como compatibilidad con dispositivos de captura de vídeo y códecs de hardware.

## <a name="format-support"></a>Compatibilidad con formatos

En Windows 7, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) amplia compatibilidad con formato que incluye códecs para vídeo *H.264,* *M JPEGEG* y *MP3*; nuevos orígenes para *MP4,* *3GP,* *audio AAC* y *AVI*; y nuevos receptores de archivos *para MP4,* *3GP* y *MP3.* (Vea [Formatos multimedia admitidos en Media Foundation).](../medfound/supported-media-formats-in-media-foundation.md)

## <a name="hardware-devices"></a>Dispositivos de hardware

[Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) ahora admite los siguientes tipos de dispositivos de hardware en la canalización de audio y vídeo:

-   *Dispositivos de captura de vídeo UVC 1.1,* como cámaras web
-   Dispositivos de captura de audio
-   Codificadores y descodificadores de hardware
-   Procesadores de vídeo de hardware, como convertidores de espacio de color

Los códecs de hardware pueden realizar una transcodificación de vídeo muy rápida. Por ejemplo, supongamos que desea transferir un archivo *Windows Media Video (WMV)* a un teléfono móvil que solo admita *archivos 3GP.* Con un codificador de hardware, el archivo se puede transcodificar "según sea necesario", inmediatamente antes de transferirlo al dispositivo.

Los dispositivos de hardware [se representan Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) mediante un objeto proxy y se usan en la canalización igual que los componentes basados en software. (Vea [Novedades de Media Foundation).](../medfound/whats-new-for-media-foundation.md)

## <a name="simplified-programming-model"></a>Modelo de programación simplificado

En Windows Vista, [Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) un conjunto de API de nivel relativamente bajo. Estas API son flexibles, pero puede que no sean adecuadas para realizar tareas. Windows 7 agrega nuevas API de alto nivel que hacen que sea más fácil escribir aplicaciones multimedia en *C++.* Estas nuevas API de alto nivel incluyen:

-   **MFPlay**. Estas API están diseñadas para la reproducción de audio y vídeo. Admiten las operaciones de reproducción típicas (detención, pausa, reproducción, búsqueda, control de velocidad, volumen de audio, etc.), a la vez que ocultan los detalles de las API de bajo nivel (las capas de sesión y topología).
-   **Lector de origen**. Puede usar estas API para extraer datos sin procesar o descodificados de un archivo multimedia, sin saber nada sobre el formato subyacente. Por ejemplo, puede obtener un mapa de bits en miniatura de un archivo de vídeo u obtener fotogramas de vídeo en directo desde una cámara web.
-   **Escritor de receptores**. Puede usar estas API para crear archivos multimedia pasando datos sin comprimir o codificados. Por ejemplo, puede volver a codificar o remezclar un archivo de vídeo.
-   **Transcodifique**. Estas API tienen como destino los escenarios de codificación de audio y vídeo más comunes.

## <a name="platform-improvements"></a>Mejoras en la plataforma

Windows 7 incluye numerosas mejoras en [](/windows/desktop/medfound/microsoft-media-foundation-sdk) las API de plataforma Media Foundation subyacentes. Las aplicaciones avanzadas pueden usar estas API directamente; otras aplicaciones obtienen las ventajas indirectamente. Entre las ventajas se incluye lo siguiente:

-   Mejoras en la canalización de vídeo para reducir el consumo de energía y el uso de memoria de vídeo.
-   Nuevas API de procesamiento de vídeo *DVXA,* que usan un modelo de composición más flexible y son más adecuadas para formatos *de vídeo hd.*
-   Mejoras en la forma en que se enumeran y administran los complementos (orígenes y descodificadores).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Media Foundation](../medfound/whats-new-for-media-foundation.md)
</dt> </dl>

 

 