---
title: Asistente para complementos de DSP
description: Asistente para complementos de DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Reproductor de Windows Media complementos, asistente para complementos
- complementos, asistente para complementos
- complementos de procesamiento de señales digitales, asistente para complementos
- Complementos de DSP, asistente para complementos
- Asistente para complementos
- Visual Studio,asistente para complementos DE DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dd9af9353b076525038a2a5df85c219d4d07c22fa3680a164ca7678393e92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839366"
---
# <a name="dsp-plug-in-wizard"></a>Asistente para complementos de DSP

El SDK Reproductor de Windows Media proporciona un asistente para complementos que puede agregar a Visual Studio. El asistente puede generar código de ejemplo para una variedad de complementos, incluidos los siguientes tipos de complementos DE DSP:

-   Complemento DSP de audio
-   Complemento DSP de audio (modo dual)
-   Complemento DSP de vídeo
-   Complemento DSP de vídeo (modo dual)

Cada uno de los dos complementos de ejemplo básicos, DSP de audio y DSP de vídeo, funciona como un objeto multimedia DirectX (DMO). Es decir, cada complemento de ejemplo implementa la **interfaz IMediaObject.** Cada uno de los dos complementos de ejemplo de modo dual puede funcionar como una DMO o como una transformación de Media Foundation (MFT). Es decir, cada complemento de ejemplo de modo dual implementa la interfaz **IMediaObject** y **la interfaz DETRANSFORMTransform.**

Puede compilar, vincular, registrar y probar el código del complemento de ejemplo. A continuación, puede modificar el código de ejemplo generado para crear su propio complemento DE DSP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de un complemento DSP**](building-a-dsp-plug-in.md)
</dt> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Actualizaciones del Asistente para complementos DE DSP para Reproductor de Windows Media 11**](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




