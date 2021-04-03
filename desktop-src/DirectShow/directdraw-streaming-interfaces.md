---
description: Interfaces de streaming de DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfaces de streaming de DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079981"
---
# <a name="directdraw-streaming-interfaces"></a>Interfaces de streaming de DirectDraw

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.

 

Si usa formatos de vídeo compatibles con DirectDraw en las secuencias, las siguientes interfaces proporcionan un control más eficaz sobre los datos que las interfaces base más genéricas.



| Interfaz                                                  | Descripción                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Establece y recupera el formato de flujo y el objeto de DirectDraw asociado al flujo multimedia. Esta interfaz se deriva de [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream). También puede usar esta interfaz para crear ejemplos de vídeo. |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Permite adjuntar ejemplos de vídeo a superficies de DirectDraw. Esta interfaz se deriva de la interfaz [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) . Cada superficie adjunta incluye un rectángulo de recorte para facilitar la representación. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



