---
description: Procesadores de señal digital
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Procesadores de señal digital
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697918"
---
# <a name="digital-signal-processors"></a>Procesadores de señal digital

En esta sección se describen los objetos de procesador de señal digital (DSP) proporcionados por Windows.

Microsoft usa el término *procesador de señal digital* para designar un conjunto de objetos com que realizan transformaciones en datos de audio y vídeo sin comprimir. Los DSP descritos en este SDK transforman audio y vídeo en diversos formatos sin comprimir.

Los DSP pueden usarse por sí solos o en combinación con los códecs de audio y vídeo. A excepción del DSP de captura de voz, cada DSP mostrado aquí implementa dos interfaces independientes pero similares.



| Interfaz                              | Descripción                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatible con Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatible con DirectShow.                 |



 

Puede configurar los DSP mediante la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para establecer propiedades. Algunos de los DSP tienen interfaces adicionales que establecen propiedades. Para utilizar estas interfaces, llame al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de cualquier otra interfaz del DSP. En el tema de referencia de cada DSP se enumeran las propiedades, interfaces y otras características admitidas.

Esta sección contiene los temas siguientes.



| DSP                                                      | Descripción                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [DSP de remuestreador de audio](audioresampler.md)                | Convierte la velocidad de muestreo de una secuencia de audio.       |
| [DSP de transformación de control de color](colorcontroltransform.md) | Ajusta las características de color de una secuencia de vídeo. |
| [DSP de convertidor de colores](colorconverter.md)                | Convierte un flujo de vídeo entre formatos de color.       |
| [DSP de convertidor de velocidad de fotogramas](framerateconverter.md)       | Cambia la velocidad de fotogramas de una secuencia de vídeo.            |
| [Vídeo de tamaño DSP](videoresizer.md)                    | Cambia el tamaño de una secuencia de vídeo.                              |
| [DSP de captura de voz](voicecapturedmo.md)                 | Encapsula varios DSP relacionados con la captura de voz.  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
