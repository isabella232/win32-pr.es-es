---
description: Objeto de streaming multimedia y jerarquía de la interfaz
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Objeto de streaming multimedia y jerarquía de la interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914229"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Objeto de streaming multimedia y jerarquía de la interfaz

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.

 

En el diagrama siguiente se muestra la jerarquía de objetos que se usa en el streaming multimedia.

![jerarquía de objetos multimediastreaming](images/mmstream02.png)

La arquitectura de transmisión por secuencias multimedia define tres tipos generales de objeto:

-   El objeto **AMMultimediaStream** expone la interfaz [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) . Internamente, este objeto ajusta el gráfico de filtros de DirectShow.
-   Los objetos de *flujo de medios* exponen la interfaz [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) y son específicos de los datos. El objeto AMMultimediaStream contiene uno o más flujos multimedia.
-   Los objetos de *ejemplo de secuencia* contienen los datos de una secuencia determinada.

Se admiten los siguientes objetos de flujo multimedia:

-   Secuencia de audio. Expone la interfaz [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .
-   Secuencia de DirectDraw. Representa una secuencia de vídeo que se representa en una superficie de DirectDraw. Expone la interfaz [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .
-   Secuencia de tipo de medio. Representa datos arbitrarios. Expone la interfaz [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .

Cada objeto de flujo multimedia crea su propio tipo de objeto de ejemplo de secuencia:

-   Secuencias de audio cree ejemplos de audio, que exponen la interfaz [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .
-   Las secuencias DirectDraw crean ejemplos de DirectDraw, que exponen la interfaz [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .
-   Los flujos de tipo de medio crean ejemplos de tipos de medios, que exponen la interfaz [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .

En el diagrama siguiente se muestra la jerarquía de la interfaz para las interfaces enumeradas anteriormente:

![jerarquía de la interfaz multimediastreaming](images/mmstream01.png)

 

 



