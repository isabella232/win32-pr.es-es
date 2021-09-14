---
description: DirectDraw Streaming Interfaces
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: DirectDraw Streaming Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062358"
---
# <a name="directdraw-streaming-interfaces"></a>DirectDraw Streaming Interfaces

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

Si usa formatos de vídeo compatibles con DirectDraw en las secuencias, las interfaces siguientes le dan un control más eficaz sobre los datos que las interfaces base más genéricas.



| Interfaz                                                  | Descripción                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Establece y recupera el formato de secuencia y el objeto DirectDraw asociado al flujo multimedia; esta interfaz se deriva de [**IMediaStream.**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) También puede usar esta interfaz para crear ejemplos de vídeo. |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Permite adjuntar ejemplos de vídeo a superficies de DirectDraw. esta interfaz deriva de la [**interfaz IStreamSample.**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) Cada superficie adjunta incluye un rectángulo de recorte para facilitar la representación. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



