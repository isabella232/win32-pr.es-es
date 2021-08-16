---
description: Interfaces de captura y representación de audio
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Interfaces de captura y representación de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ffdf586ec8566abddadcb0b7109680664963a63071472a3ac7aa895981e643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824255"
---
# <a name="audio-capture-and-rendering-interfaces"></a>Interfaces de captura y representación de audio

Estas interfaces admiten la captura y representación de audio en DirectShow



| Interfaz                                              | Descripción                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | Acceda a las entradas análogas en la tarjeta de sonido del sistema y ajuste características, como mono o estéreo, nivel de mezcla, nivel de panorámica, sonoridad, triple y sonido. |
| [**IAMAudioRendererStats**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | Obtenga información estadística de rendimiento sobre el representador de audio.                                                                                          |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | Controlar cómo el filtro de captura de audio asigna búferes.                                                                                                   |
| [**IAMClockLockLockE**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | Controlar la tolerancia de un representador de audio cuando coincide con las velocidades con otro reloj.                                                                      |
| [**IAMDirect Sound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | Permite a una aplicación especificar qué ventana tiene el foco para controlar la reproducción de audio Direct Sound.                                                      |
| [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | Mantenga un recurso de dispositivo de audio antes de que sea necesario.                                                                                                        |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | Consulte y establezca el formato de salida del filtro de captura.                                                                                                         |
| [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | Establecer el volumen y el equilibrio de salida de audio.                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 



