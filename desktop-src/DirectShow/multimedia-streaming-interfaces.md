---
description: Interfaces de streaming multimedia
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Interfaces de streaming multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d654bae73ee822f553a1494e3b374cf35b8ac4a1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547438"
---
# <a name="multimedia-streaming-interfaces"></a>Interfaces de streaming multimedia

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.

 

Esta sección contiene entradas de referencia para todas las interfaces de streaming multimedia y sus métodos, incluidos los que admite Microsoft DirectShow.



| Interfaz                                                  | Descripción                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | Controla las conexiones internas entre filtros de DirectShow y gráficos de filtro en aplicaciones que usan streaming multimedia.                            |
| [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Contiene métodos para manipular ejemplos de secuencias con tipos de medios arbitrarios.                                                                            |
| [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Contiene métodos para crear flujos multimedia con tipos de medios arbitrarios.                                                                            |
| [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | Expone la funcionalidad de DirectShow a los desarrolladores de flujos multimedia.                                                                                       |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | Proporciona métodos que permiten a las aplicaciones establecer y obtener los datos de audio subyacentes a los que hará referencia las secuencias de audio.                                   |
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | Controla los flujos multimedia de audio proporcionando métodos que establecen y obtienen el formato de la secuencia.                                                                 |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | Recupera información de los objetos de datos [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) subyacentes.                                                                |
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Controla las secuencias multimedia que aparecen en las superficies® de DirectDraw de Microsoft®.                                                                                  |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Proporciona métodos que establecen y recuperan punteros a la superficie de DirectDraw asociada al ejemplo de secuencia actual.                                    |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | Proporciona acceso a las características de un flujo multimedia, como el tipo de medio y el ID. de propósito de la secuencia. También tiene métodos que crean ejemplos de datos. |
| [**IMediaStreamFilter**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | Compatible con el filtro de flujo de medios, que usa internamente el objeto de flujo multimedia. .                                                       |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | Contiene métodos que establecen y recuperan datos de memoria en objetos de datos de audio.                                                                               |
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | Proporciona métodos que controlan una secuencia multimedia y proporcionan acceso a sus flujos multimedia subyacentes.                                                   |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | Proporciona control sobre el comportamiento de los ejemplos de secuencias.                                                                                                   |



 

 

 



