---
description: Audio Streaming Interfaces
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Audio Streaming Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1087ab127258fcd4f587cdd029d4604c35524689b5f0877476e1137e2ed924eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824475"
---
# <a name="audio-streaming-interfaces"></a>Audio Streaming Interfaces

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 



| Interfaz                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Controla las secuencias multimedia de audio. Esta interfaz hereda de la [**interfaz IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) y se usa para crear uno o varios [**objetos IAudioStreamSample.**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) También se usa para establecer y recuperar el formato actual de los datos de flujo.                                                                                                            |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Recupera información de los objetos de datos [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) subyacentes.                                                                                                                                                                                                                                                                                                        |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Contiene métodos que establecen y recuperan datos de memoria en objetos de datos de audio. Los objetos de datos de audio proporcionan los datos subyacentes a los que acceden los ejemplos de secuencia. Esta interfaz proporciona una manera de inicializar búferes de memoria y de establecer cantidades reales de datos de audio en los objetos . Además, el [**método IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) se puede usar para recuperar datos de memoria de audio. |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Proporciona métodos que permiten a las aplicaciones establecer y obtener los datos de audio subyacentes a los que harán referencia las secuencias de audio. El formato de datos de audio se establece en la [**estructura DEDATOSATEX.**](/previous-versions/dd757713(v=vs.85))                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
