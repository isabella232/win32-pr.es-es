---
description: Procesadores de señal digital
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Procesadores de señal digital
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f5c9aa0ee3c4cc2a8c7f725b3a8444f4852c8c5b52ee3713b533ec435f4a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100947"
---
# <a name="digital-signal-processors"></a>Procesadores de señal digital

En esta sección se describen los objetos del procesador de señales digitales (DSP) proporcionados por Windows.

Microsoft usa el término *procesador de señales digitales* para designar un conjunto de objetos COM que realizan transformaciones en datos de audio y vídeo sin comprimir. Los DSP descritos en este SDK transforman audio y vídeo en una variedad de formatos sin comprimir.

Los DSP se pueden usar por sí mismos o en combinación con códecs de audio y vídeo. A excepción del DSP de captura de voz, cada DSP enumerado aquí implementa dos interfaces independientes pero similares.



| Interfaz                              | Descripción                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatible con Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatible con DirectShow.                 |



 

Puede configurar los DSP mediante la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para establecer propiedades. Algunos de los DSP tienen interfaces adicionales que establecen propiedades. Para usar estas interfaces, llame al [**método QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de cualquier otra interfaz del DSP. En el tema de referencia de cada DSP se enumeran las propiedades, interfaces y otras características admitidas.

Esta sección contiene los temas siguientes.



| Dsp                                                      | Descripción                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [Audio Resampler DSP](audioresampler.md)                | Convierte la frecuencia de muestreo de una secuencia de audio.       |
| [DSP de transformación de control de color](colorcontroltransform.md) | Ajusta las características de color de una secuencia de vídeo. |
| [DSP de convertidor de colores](colorconverter.md)                | Convierte una secuencia de vídeo entre formatos de color.       |
| [DSP del convertidor de velocidad de fotogramas](framerateconverter.md)       | Cambia la velocidad de fotogramas de una secuencia de vídeo.            |
| [DSP de cambio de tamaño de vídeo](videoresizer.md)                    | Cambia el tamaño de una secuencia de vídeo.                              |
| [DSP de captura de voz](voicecapturedmo.md)                 | Encapsula varios DSP relacionados con la captura de voz.  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
