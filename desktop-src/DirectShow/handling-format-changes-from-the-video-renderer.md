---
description: Control de cambios de formato desde el representador de vídeo
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: Control de cambios de formato desde el representador de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d731ac4b9d6985cf5ad92f642b6d8262209fa91d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169950"
---
# <a name="handling-format-changes-from-the-video-renderer"></a>Control de cambios de formato desde el representador de vídeo

En esta sección se describe cómo un filtro descodificador o filtro de transformación debe controlar los cambios de formato del representador de vídeo.

**Filtro de representador de vídeo**

Cuando se conecta [el filtro Antiguo](video-renderer-filter.md) representador de vídeo, requiere un formato RGB que coincida con el formato de presentación del monitor principal. Esto le permite usar GDI para la representación si DirectDraw no está disponible. Cuando se inicia la reproducción, el representador de vídeo puede cambiar a un formato compatible con DirectDraw. Para comprobar si el filtro ascendente puede admitir el nuevo formato, el representador de vídeo llama a [**IPin::QueryAccept en**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) el pin de salida del filtro ascendente. Si el filtro ascendente acepta el nuevo formato, el **método QueryAccept** devuelve S \_ OK. El representador de vídeo cambia los formatos adjuntando un tipo de medio con el nuevo formato al siguiente ejemplo multimedia devuelto por su asignador. El filtro ascendente debe comprobar los cambios de formato llamando a [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) en cada ejemplo. El representador de vídeo puede cambiar entre el formato original y el nuevo formato en cualquier momento durante el streaming. No llama a **QueryAccept después** del primer cambio de formato. Una vez que el filtro ascendente ha aceptado el nuevo formato, debe poder cambiar de un lado a otro.

El filtro ascendente puede rechazar el cambio de formato devolviendo S \_ FALSE desde **QueryAccept**. En ese caso, el representador de vídeo sigue utilizando GDI con el formato original.

**Filtro de representador de mezcla de vídeo**

El filtro Representador de mezcla de vídeo (VMR-7 y VMR-9) se conectará con cualquier formato que sea compatible con el hardware gráfico del sistema. VMR-7 siempre usa DirectDraw para la representación y asigna las superficies subyacentes de DirectDraw cuando se conecta el filtro ascendente. VMR-9 siempre usa Direct3D para la representación y asigna las superficies subyacentes de Direct3D cuando se conecta el filtro ascendente.

El hardware gráfico puede requerir un paso de superficie mayor que el ancho de la imagen. En ese caso, el VMR solicita un nuevo formato mediante una llamada a **QueryAccept**. Notifica el paso de superficie en el **miembro biWidth** de [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en formato de vídeo. Si el filtro ascendente no devuelve S OK de \_ **QueryAccept,** el VMR rechaza el formato e intenta conectarse con el siguiente formato anunciado por el filtro ascendente. VmR asocia el tipo de medio con el nuevo formato al primer ejemplo multimedia. Después del primer ejemplo, el formato permanece constante; El VMR no cambia de formato mientras se ejecuta el gráfico.

**Representación de vídeo mejorada (EVR)**

El EVR siempre usa Direct3D para la representación. Si se necesita un paso de superficie mayor, el EVR usa el mismo mecanismo **QueryAccept** que el VMR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[QueryAccept (upstream)](queryaccept--upstream.md)
</dt> </dl>

 

 



