---
title: Interfaces de XAudio2
description: Esta sección contiene información sobre las interfaces proporcionadas por la API de Microsoft XAudio2.
ms.assetid: 96691e00-9ed0-b31c-fbe9-4daaba0daf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d9f2c777a7b98c5cbc78a130c0a1431be5971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279365"
---
# <a name="xaudio2-interfaces"></a>Interfaces de XAudio2

Esta sección contiene información sobre las interfaces proporcionadas por la API de Microsoft XAudio2.

## <a name="in-this-section"></a>En esta sección



| Tema                                                               | Descripción                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                             | IXAudio2 es la interfaz para el objeto [XAudio2](xaudio2-apis-portal.md) que administra todos los Estados del motor de audio, el subproceso de procesamiento de audio, el gráfico de voz, etc. <br/>                                                                                                                                                |
| [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice)<br/>                   | [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice) representa la interfaz base de la que se derivan [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice), [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) y [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) . Los métodos que se enumeran a continuación son comunes a todas las subclases de voz.<br/> |
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)<br/>       | Use una voz de origen para enviar datos de audio a la canalización de procesamiento de XAudio2.<br/>                                                                                                                                                                                                                                                   |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)<br/>       | Una voz de submezcla se usa principalmente para mejorar el rendimiento y el procesamiento de efectos. <br/>                                                                                                                                                                                                                                        |
| [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)<br/> | Se utiliza una voz de maestro para representar el dispositivo de salida de audio.<br/>                                                                                                                                                                                                                                                               |
| [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)<br/> | La interfaz IXAudio2EngineCallback contiene métodos que notifican al cliente cuando se producen determinados eventos en el motor [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .<br/>                                                                                                                                                                           |
| [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)<br/>   | La interfaz [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contiene métodos que notifican al cliente cuando se producen determinados eventos en un [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)determinado. <br/>                                                                                                                       |
| [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)<br/>                                   | La interfaz para un objeto de procesamiento de audio que se utiliza en una cadena de efectos de XAudio2.<br/>                                                                                                                                                                                                                                        |
| [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)<br/>               | Una interfaz opcional que permite a un XAPO usar parámetros específicos del efecto.<br/>                                                                                                                                                                                                                                                  |
| [**IXAPOHrtfParameters**](/windows/win32/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters)<br/>       | La interfaz que se usa para establecer los parámetros que controlan cómo se aplica la función de transferencia relacionada con el encabezado (HRTF) a un sonido.<br/>                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> <dt>

[Referencia de programación](./programming-reference.md)
</dt> </dl>

 

 
