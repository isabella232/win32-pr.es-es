---
title: Interfaces XAudio2
description: Esta sección contiene información sobre las interfaces proporcionadas por la API de Microsoft XAudio2.
ms.assetid: 96691e00-9ed0-b31c-fbe9-4daaba0daf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d9f2c777a7b98c5cbc78a130c0a1431be5971d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571944"
---
# <a name="xaudio2-interfaces"></a>Interfaces XAudio2

Esta sección contiene información sobre las interfaces proporcionadas por la API de Microsoft XAudio2.

## <a name="in-this-section"></a>En esta sección



| Tema                                                               | Descripción                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                             | IXAudio2 es la interfaz del objeto [XAudio2](xaudio2-apis-portal.md) que administra todos los estados del motor de audio, el subproceso de procesamiento de audio, el gráfico de voz, etc. <br/>                                                                                                                                                |
| [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice)<br/>                   | [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice) representa la interfaz base de la que [**se derivan IXAudio2SourceVoice,**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) e [**IXAudio2MasteringVoice.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) Los métodos enumerados a continuación son comunes a todas las subclases de voz.<br/> |
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)<br/>       | Use una voz de origen para enviar datos de audio a la canalización de procesamiento de XAudio2.<br/>                                                                                                                                                                                                                                                   |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)<br/>       | Una voz de submezcla se usa principalmente para las mejoras de rendimiento y el procesamiento de efectos. <br/>                                                                                                                                                                                                                                        |
| [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)<br/> | Se usa una voz maestra para representar el dispositivo de salida de audio.<br/>                                                                                                                                                                                                                                                               |
| [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)<br/> | La interfaz IXAudio2EngineCallback contiene métodos que notifican al cliente cuándo se suceden determinados eventos en el [**motor IXAudio2.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                                                                                                                                                                           |
| [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)<br/>   | La [**interfaz IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) contiene métodos que notifican al cliente cuándo se suceden determinados eventos en un [**IXAudio2SourceVoice determinado.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) <br/>                                                                                                                       |
| [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)<br/>                                   | Interfaz de un objeto de procesamiento de audio que se usa en una cadena de efectos XAudio2.<br/>                                                                                                                                                                                                                                        |
| [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)<br/>               | Interfaz opcional que permite que un XAPO use parámetros específicos del efecto.<br/>                                                                                                                                                                                                                                                  |
| [**IXAPOHrtfParameters**](/windows/win32/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters)<br/>       | Interfaz que se usa para establecer parámetros que controlan cómo se aplica la función de transferencia relacionada con la cabeza (HRTF) a un sonido.<br/>                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> <dt>

[Referencia de programación](./programming-reference.md)
</dt> </dl>

 

 
