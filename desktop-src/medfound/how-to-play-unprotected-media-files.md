---
description: En este tutorial se muestra cómo reproducir archivos multimedia mediante el objeto de sesión de medios.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Cómo reproducir archivos multimedia con Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104551624"
---
# <a name="how-to-play-media-files-with-media-foundation"></a>Cómo reproducir archivos multimedia con Media Foundation

En este tutorial se muestra cómo reproducir archivos multimedia mediante el objeto de [sesión de medios](media-session.md) .

## <a name="prerequisites"></a>Requisitos previos

Antes de leer este tema, debe estar familiarizado con los siguientes conceptos de Media Foundation:

-   [Sesión de medios](media-session.md)
-   [Solucionador de origen](source-resolver.md)
-   [Topologías](topologies.md)
-   [Generadores de eventos multimedia](media-event-generators.md)
-   [Descriptores de presentación](presentation-descriptors.md)

> [!Note]  
> En este tema no se describe cómo reproducir archivos protegidos con la administración de derechos digitales (DRM). Para obtener información acerca de DRM en Microsoft Media Foundation, consulte [Cómo reproducir archivos multimedia protegidos](how-to-play-protected-media-files.md).

 

## <a name="overview"></a>Información general

Los objetos siguientes se usan para reproducir un archivo multimedia con la sesión multimedia:

-   Un *origen multimedia* es un objeto que analiza un archivo multimedia u otro origen de datos multimedia. El origen de medios crea objetos de *secuencia* para cada secuencia de audio o vídeo del archivo. Los *descodificadores* convierten los datos multimedia codificados en vídeo y audio sin comprimir.
-   La *resolución de origen* crea un origen multimedia a partir de una dirección URL.
-   El [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR) representa el vídeo en la pantalla.
-   [Streaming audio renderer](streaming-audio-renderer.md) (SAR) representa el audio en un altavoz u otro dispositivo de salida de audio.
-   Una *topología* define el flujo de datos desde el origen de medios hasta EVR y SAR.
-   La *sesión multimedia* controla el flujo de datos y envía los eventos de estado a la aplicación. En el siguiente diagrama se muestra este proceso.

![diagrama que muestra la reproducción mediante la sesión multimedia](images/session-playback.gif)

A continuación se describe un esquema general de los pasos necesarios para reproducir un archivo multimedia mediante la sesión multimedia:

1.  Llame a la función [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar la plataforma Media Foundation.
2.  Llame a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para crear una nueva instancia de la sesión multimedia.
3.  Utilice el solucionador de origen para crear un origen de medios. Para obtener más información, vea [usar el solucionador de origen](using-the-source-resolver.md).
4.  Cree una topología que conecte el origen multimedia a EVR y SAR. En este paso, la aplicación crea una topología *parcial* que no incluye los descodificadores. Para obtener más información, consulte [crear topologías de reproducción](creating-playback-topologies.md).
5.  Llame a [**IMFMediaSession:: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para establecer la topología en la sesión multimedia.
6.  Use la interfaz [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) para obtener los eventos de la sesión multimedia.
7.  Llame a [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar la reproducción. Una vez iniciada la reproducción, puede pausarla llamando a [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), o bien detenerla llamando a [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
8.  Cuando se cierra la aplicación, libera los recursos:

    1.  Llame a [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para cerrar la sesión multimedia. Este método es asincrónico. Cuando se completa, la sesión multimedia envía un evento [MESessionClosed](mesessionclosed.md) . Después, es seguro realizar los pasos restantes.
    2.  Llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para cerrar el origen del medio.
    3.  Llame a [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) para cerrar la sesión multimedia.
    4.  Llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para cerrar la plataforma Media Foundation.

En las secciones siguientes se muestra un ejemplo de código completo:

-   [Paso 1: declarar la clase CPlayer](step-1--declare-the-cplayer-class.md)
-   [Paso 2: crear el objeto CPlayer](step-2--create-the-cplayer-object.md)
-   [Paso 3: abrir un archivo multimedia](step-3--open-a-media-file.md)
-   [Paso 4: crear la sesión multimedia](step-4--create-the-media-session.md)
-   [Paso 5: controlar los eventos de la sesión multimedia](step-5--handle-media-session-events.md)
-   [Paso 6: control de la reproducción](step-6--control-playback.md)
-   [Paso 7: apagar la sesión multimedia](step-7--shut-down-the-media-session.md)
-   [Ejemplo de reproducción de sesión multimedia](media-session-playback-example.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> <dt>

[Reproducción de audio y vídeo](audio-video-playback.md)
</dt> </dl>

 

 



