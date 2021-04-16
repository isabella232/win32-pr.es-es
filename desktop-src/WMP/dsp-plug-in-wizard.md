---
title: Asistente para complementos de DSP
description: Asistente para complementos de DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Complementos de Windows Media Player, Asistente para complementos
- complementos, Asistente para complementos
- Complementos de procesamiento de señal digital, Asistente para complementos
- Complementos DSP, Asistente para complementos
- Asistente para complementos
- Visual Studio, Asistente para complementos de DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532079"
---
# <a name="dsp-plug-in-wizard"></a>Asistente para complementos de DSP

El SDK de Windows Media Player proporciona un asistente para complementos que puede Agregar a Visual Studio. El asistente puede generar código de ejemplo para una variedad de complementos, incluidos los siguientes tipos de complementos de DSP:

-   Complemento DSP de audio
-   Complemento DSP de audio (modo dual)
-   Complemento DSP de vídeo
-   Complemento DSP de vídeo (modo dual)

Cada uno de los dos complementos de ejemplo básicos, DSP de audio y vídeo DSP, funciona como un objeto multimedia de DirectX (DMO). Es decir, cada complemento de ejemplo implementa la interfaz **IMediaObject** . Cada uno de los dos complementos de ejemplo de doble modo puede funcionar como DMO o como una transformación de Media Foundation (MFT). Es decir, cada complemento de ejemplo de dos modos implementa la interfaz **IMediaObject** y la interfaz **IMFTransform** .

Puede compilar, vincular, registrar y probar el código del complemento de ejemplo. Después, puede modificar el código de ejemplo generado para crear su propio complemento DSP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear un complemento DSP**](building-a-dsp-plug-in.md)
</dt> <dt>

[**Introducción al desarrollador de complementos de DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Actualizaciones del Asistente para complementos de DSP para Windows Media Player 11**](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




