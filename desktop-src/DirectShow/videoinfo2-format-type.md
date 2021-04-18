---
description: Tipo de formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo de formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687166"
---
# <a name="videoinfo2-format-type"></a>Tipo de formato VideoInfo2

Un tipo de medio preferido del PIN de vista previa puede ser un tipo con un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Esta estructura de formato admite características especiales como el vídeo entrelazado y las relaciones de aspecto de la imagen.

VMR-7 y VMR-9 admiten [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directamente. Al conectar la VMR al descodificador, se negociará el mejor formato. El filtro de representador de vídeo anterior, sin embargo, no es compatible con **VIDEOINFOHEADER2**. Para usar los tipos de formato **VIDEOINFOHEADER2** con el filtro de representador de vídeo, debe insertar el filtro de [mezclador de superposición](overlay-mixer-filter.md) en el gráfico.

1.  Enumerar los tipos de medios preferidos en el PIN de salida del filtro del descodificador, mediante el método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .
2.  Compruebe el primer tipo de medio en la secuencia de enumeración.
3.  Si el tipo de formato es **format \_ VideoInfo2**, conecte el PIN de salida al mezclador de superposición. A continuación, conecte el mezclador de superposición al representador de vídeo. (Consulte [pines del puerto de vídeo](video-port-pins.md)).

Si no le importa estas características, no tiene que usar el mezclador de superposición. Conecte el descodificador directamente al representador de vídeo y se conectará con un formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en su lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Usar el mezclador de superposición en la captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



