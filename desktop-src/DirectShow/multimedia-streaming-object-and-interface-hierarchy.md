---
description: Jerarquía de interfaz y objetos de streaming multimedia
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Jerarquía de interfaz y objetos de streaming multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254318"
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

 

 



