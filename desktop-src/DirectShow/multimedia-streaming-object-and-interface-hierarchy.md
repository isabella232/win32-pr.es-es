---
description: Jerarquía de interfaz y objetos de streaming multimedia
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Jerarquía de interfaz y objetos de streaming multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73da4777c2d05ff6455758ebde6e64a9a4c8277e8445ed59dca7f17088baea0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075783"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Jerarquía de interfaz y objetos de streaming multimedia

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

En el diagrama siguiente se muestra la jerarquía de objetos utilizada en el streaming multimedia.

![jerarquía de objetos multimediastreaming](images/mmstream02.png)

La arquitectura de streaming multimedia define tres tipos generales de objeto:

-   El **objeto AMMultimediaStream** expone la [**interfaz IAMMultiMediaStream.**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) Internamente, este objeto encapsula el DirectShow gráfico de filtros.
-   *Los objetos de secuencia* multimedia exponen [**la interfaz IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) y son específicos de los datos. El objeto AMMultimediaStream contiene uno o varios flujos multimedia.
-   *Los objetos de* ejemplo de secuencia contienen los datos de una secuencia determinada.

Se admiten los siguientes objetos de flujo multimedia:

-   Secuencia de audio. Expone la [**interfaz IAudioMediaStream.**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)
-   Secuencia de DirectDraw. Representa una secuencia de vídeo que se representa en una superficie de DirectDraw. Expone la [**interfaz IDirectDrawMediaStream.**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)
-   Secuencia de tipo de medio. Representa datos arbitrarios. Expone la [**interfaz IAMMediaTypeStream.**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)

Cada objeto de secuencia multimedia crea su propio tipo de objeto de ejemplo de secuencia:

-   Las secuencias de audio crean ejemplos de audio, que exponen la [**interfaz IAudioStreamSample.**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)
-   Las secuencias de DirectDraw crean ejemplos de DirectDraw, que exponen la [**interfaz IDirectDrawStreamSample.**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample)
-   Las secuencias de tipo multimedia crean ejemplos de tipo multimedia, que exponen [**la interfaz IAMMediaTypeSample.**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)

En el diagrama siguiente se muestra la jerarquía de interfaces para las interfaces enumeradas anteriormente:

![jerarquía de interfaz de multimediastreaming](images/mmstream01.png)

 

 



