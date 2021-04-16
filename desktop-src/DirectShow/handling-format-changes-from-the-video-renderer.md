---
description: Control de los cambios de formato del representador de vídeo
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: Control de los cambios de formato del representador de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d731ac4b9d6985cf5ad92f642b6d8262209fa91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105652313"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>Control de los cambios de formato del representador de vídeo

En esta sección se describe cómo un filtro de descodificador o de transformación debe controlar los cambios de formato del representador de vídeo.

**Filtro de representador de vídeo**

Cuando se conecta el filtro de [representador de vídeo](video-renderer-filter.md) anterior, se requiere un formato RGB que coincida con el formato de presentación del monitor principal. Esto le permite usar GDI para la representación si DirectDraw no está disponible. Cuando se inicia la reproducción, el representador de vídeo puede cambiar a un formato compatible con DirectDraw. Para verfify si el filtro de nivel superior puede admitir el nuevo formato, el representador de vídeo llama a [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de salida del filtro de nivel superior. Si el filtro de nivel superior acepta el nuevo formato, el método **QueryAccept** devuelve S \_ correcto. El representador de vídeo cambia de formato adjuntando un tipo de medio con el nuevo formato al siguiente ejemplo multimedia devuelto por su asignador. El filtro de nivel superior debe comprobar los cambios de formato llamando a [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) en cada ejemplo. El representador de vídeo puede alternar entre el formato original y el nuevo formato en cualquier momento durante el streaming. No llama a **QueryAccept** después del primer cambio de formato. Una vez que el filtro de nivel superior ha aceptado el nuevo formato, debe ser capaz de cambiar de un y otro.

El filtro de nivel superior puede rechazar el cambio de formato devolviendo S \_ false desde **QueryAccept**. En ese caso, el representador de vídeo sigue usando GDI con el formato original.

**Filtro de representador de combinación de vídeo**

El filtro de representador de combinación de vídeo (VMR-7 y VMR-9) se conectará con cualquier formato compatible con el hardware de gráficos del sistema. VMR-7 siempre usa DirectDraw para la representación y asigna las superficies de DirectDraw subyacentes cuando se conecta el filtro de nivel superior. VMR-9 siempre usa Direct3D para la representación y asigna las superficies de Direct3D subyacentes cuando se conecta el filtro de nivel superior.

El hardware gráfico puede requerir un intervalo mayor de superficie que el ancho de la imagen. En ese caso, la VMR solicita un nuevo formato mediante una llamada a **QueryAccept**. Notifica el intervalo de la superficie en el miembro **biwidth** del [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en el formato de vídeo. Si el filtro de nivel superior no devuelve S \_ correctos de **QueryAccept**, la VMR rechaza el formato e intenta conectarse con el siguiente formato anunciado por el filtro de nivel superior. VMR asocia el tipo de medio con el nuevo formato al primer ejemplo multimedia. Después del primer ejemplo, el formato permanece constante. VMR no cambiará de formato mientras el gráfico se esté ejecutando.

**Representación de vídeo mejorada (EVR)**

EVR siempre usa Direct3D para la representación. Si se necesita un paso de superficie mayor, el EVR usa el mismo mecanismo de **QueryAccept** que la VMR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[QueryAccept (ascendente)](queryaccept--upstream.md)
</dt> </dl>

 

 



