---
description: Interfaces de representación y captura de audio
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfaces de representación y captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677183"
---
# <a name="audio-capture-and-rendering-interfaces"></a>Interfaces de representación y captura de audio

Estas interfaces admiten la captura y representación de audio en DirectShow



| Interfaz                                              | Descripción                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | Obtener acceso a las entradas analógicas de la tarjeta de sonido del sistema y ajustar características, como mono o estéreo, nivel de combinación, nivel de pan, sonoridad, agudos y graves. |
| [**IAMAudioRendererStats**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | Obtenga información estadística sobre el rendimiento de renderering de audio.                                                                                          |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | Controlan cómo el filtro de captura de audio asigna los búferes.                                                                                                   |
| [**IAMClockSlave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | Controlar la tolerancia de un representador de audio cuando coincide con las tarifas con otro reloj.                                                                      |
| [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | Permite a una aplicación especificar qué ventana tiene el foco para controlar la reproducción de audio de DirectSound.                                                      |
| [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | Conserve un recurso de dispositivo de audio antes de que sea necesario.                                                                                                        |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | Consulta y establece el formato de salida del filtro de captura.                                                                                                         |
| [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | Establezca el volumen y el equilibrio de salida de audio.                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 



