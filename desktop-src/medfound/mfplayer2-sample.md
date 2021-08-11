---
description: Importante en desuso.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Ejemplo de MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ead2df415af1584f34661a0c1d18751350d59bd1a94ac48f41d3bf9dca2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241741"
---
# <a name="mfplayer2-sample"></a>Ejemplo de MFPlayer2

> [!IMPORTANT]
> En desuso. Esta API puede quitarse de futuras versiones de Windows. Las aplicaciones deben usar la [sesión multimedia para](media-session.md) la reproducción.

 

Muestra algunas de las características de reproducción que se omiten en el [ejemplo simplePlay,](simpleplay-sample.md) como:

-   Buscando
-   Control de velocidad (avance rápido y rebobinado)
-   Controles de volumen de audio y exclusión mutua
-   Zoom de vídeo

En la imagen siguiente se muestran los controles usados para estas características.

![captura de pantalla del ejemplo mfplayer ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las siguientes API.

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [**IAudioSessionManager**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de github Windows ejemplos clásicos](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Uso de MFPlay para la reproducción de audio y vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
