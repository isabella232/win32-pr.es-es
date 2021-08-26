---
title: Acerca de la asignación de recursos de streaming
description: Acerca de la asignación de recursos de streaming
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Reproductor de Windows Media complementos, DSP de audio
- complementos, DSP de audio
- complementos de procesamiento de señal digital, recursos de streaming de audio
- Complementos de DSP, recursos de streaming de audio
- complementos de DSP de audio, recursos de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f815fe9875f2e93e140b577da6e00dd7c684c1fedbad13234ecfbf87ca84ddb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903735"
---
# <a name="about-allocating-streaming-resources"></a>Acerca de la asignación de recursos de streaming

El complemento DSP de ejemplo generado por el asistente Reproductor de Windows Media complemento no requiere búferes de streaming adicionales. Sin embargo, es posible que desee asignar recursos de memoria para el complemento DSP. Por ejemplo, un complemento que produce un efecto de eco requeriría un búfer secundario para crear el retraso de tiempo necesario.

La **interfaz IMediaObject** contiene dos métodos para controlar esta situación. Reproductor de Windows Media llama **a IMediaObject::AllocateStreamingResources para** darle la oportunidad de crear los búferes que necesite. Reproductor de Windows Media más adelante llama a **IMediaObject::FreeStreamingResources** para permitirle liberar la memoria que asignó anteriormente. La implementación del complemento DSP de ejemplo también llama a **FreeStreamingResources** desde *CProjectName*::**FinalRelease** para asegurarse de que todos los recursos se liberan antes de que se destruya el objeto de complemento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento DSP de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




