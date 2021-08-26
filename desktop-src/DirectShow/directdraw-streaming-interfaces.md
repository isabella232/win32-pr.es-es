---
description: DirectDraw Streaming Interfaces
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: DirectDraw Streaming Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11e7eec0ec7ad82c0046b8c052ff00093b496c05495ec38590d201724d7620e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983055"
---
# <a name="directdraw-streaming-interfaces"></a>DirectDraw Streaming Interfaces

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

Si usa formatos de vídeo compatibles con DirectDraw en las secuencias, las interfaces siguientes le dan un control más eficaz sobre los datos que las interfaces base más genéricas.



| Interfaz                                                  | Descripción                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Establece y recupera el formato de secuencia y el objeto DirectDraw asociado a la secuencia multimedia. esta interfaz se deriva de [**IMediaStream.**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) También puede usar esta interfaz para crear ejemplos de vídeo. |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Permite adjuntar ejemplos de vídeo a superficies de DirectDraw; esta interfaz se deriva de la [**interfaz IStreamSample.**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) Cada superficie adjunta incluye un rectángulo de recorte para facilitar la representación. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



