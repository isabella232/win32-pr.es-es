---
title: Acerca de la asignación de recursos de streaming
description: Acerca de la asignación de recursos de streaming
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, recursos de streaming de audio
- Complementos DSP, recursos de streaming de audio
- Complementos de DSP de audio, recursos de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba82f150908e7b96f4e6e56c2161e1b2fdfe145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148833"
---
# <a name="about-allocating-streaming-resources"></a>Acerca de la asignación de recursos de streaming

El complemento DSP de ejemplo generado por el Asistente para complementos de Windows Media Player no requiere ningún búfer de streaming adicional. Sin embargo, es posible que desee asignar recursos de memoria para el complemento DSP. Por ejemplo, un complemento que genera un efecto de eco requeriría un búfer secundario para crear el retraso de tiempo necesario.

La interfaz **IMediaObject** contiene dos métodos para controlar esta situación. Windows Media Player llama a **IMediaObject:: AllocateStreamingResources** para ofrecerle la oportunidad de crear los búferes que necesite. Windows Media Player llama posteriormente a **IMediaObject:: FreeStreamingResources** para que pueda liberar cualquier memoria que haya asignado previamente. La implementación del complemento DSP de ejemplo también llama a **FreeStreamingResources** desde *CProjectName*::**FinalRelease** para asegurarse de que se liberen todos los recursos antes de que se destruya el objeto de complemento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar un complemento de DSP de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




