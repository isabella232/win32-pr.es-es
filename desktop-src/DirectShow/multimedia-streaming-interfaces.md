---
description: Multimedia Streaming Interfaces
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Multimedia Streaming Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d654bae73ee822f553a1494e3b374cf35b8ac4a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254319"
---
# <a name="multimedia-streaming-interfaces"></a>Multimedia Streaming Interfaces

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

Esta sección contiene entradas de referencia para todas las interfaces de streaming multimedia y sus métodos, incluidas las que admite Microsoft DirectShow.



| Interfaz                                                  | Descripción                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | Controla las conexiones internas entre DirectShow filtros y gráficos de filtro en aplicaciones que usan streaming multimedia.                            |
| [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Contiene métodos para manipular ejemplos de secuencias con tipos de medios arbitrarios.                                                                            |
| [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Contiene métodos para crear secuencias multimedia con tipos de medios arbitrarios.                                                                            |
| [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | Expone la funcionalidad DirectShow a los desarrolladores de secuencias multimedia.                                                                                       |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | Proporciona métodos que permiten a las aplicaciones establecer y obtener los datos de audio subyacentes a los que se hará referencia a las secuencias de audio.                                   |
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | Controla las secuencias multimedia de audio proporcionando métodos que establecen y obtienen el formato de la secuencia.                                                                 |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | Recupera información de los objetos de datos [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) subyacentes.                                                                |
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Controla los flujos multimedia que aparecen en las superficies ® DirectDraw® Microsoft.                                                                                  |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Proporciona métodos que establecen y recuperan punteros a la superficie de DirectDraw asociada al ejemplo de flujo actual.                                    |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | Proporciona acceso a las características de un flujo multimedia, como el tipo de medio y el identificador de propósito de la secuencia. También tiene métodos que crean ejemplos de datos. |
| [**IMediaStreamFilter**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | Compatible con el filtro Flujo multimedia, que el objeto de secuencia multimedia usa internamente. .                                                       |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | Contiene métodos que establecen y recuperan datos de memoria en objetos de datos de audio.                                                                               |
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | Proporciona métodos que controlan una secuencia multimedia y proporcionan acceso a sus secuencias multimedia subyacentes.                                                   |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | Proporciona control sobre el comportamiento de los ejemplos de flujo.                                                                                                   |



 

 

 



