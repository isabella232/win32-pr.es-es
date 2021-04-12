---
description: Interfaces de streaming de audio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfaces de streaming de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538014"
---
# <a name="audio-streaming-interfaces"></a>Interfaces de streaming de audio

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.

 



| Interfaz                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Controla los flujos multimedia de audio. Esta interfaz hereda de la interfaz [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) y se usa para crear uno o más objetos [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) . También se usa para establecer y recuperar el formato actual de los datos de la secuencia.                                                                                                            |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Recupera información de los objetos de datos [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) subyacentes.                                                                                                                                                                                                                                                                                                        |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Contiene métodos que establecen y recuperan datos de memoria en objetos de datos de audio. Los objetos de datos de audio proporcionan los datos subyacentes que tienen acceso a los ejemplos de secuencias. Esta interfaz proporciona una manera de inicializar los búferes de memoria y establecer la cantidad real de datos de audio en los objetos. Además, se puede usar el método [**IMemoryData:: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) para recuperar los datos de la memoria de audio. |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Proporciona métodos que permiten a las aplicaciones establecer y obtener los datos de audio subyacentes a los que hará referencia las secuencias de audio. El formato de datos de audio se establece en la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
