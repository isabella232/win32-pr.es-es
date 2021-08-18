---
description: Tipo de formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo de formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a820ea6a53c457d2d000be8b4c0e8966213c1aeeb2b5f55a780c4801a4182907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071929"
---
# <a name="videoinfo2-format-type"></a>Tipo de formato VideoInfo2

El tipo de medio preferido de un pin de vista previa podría ser un tipo con un [**formato VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Esta estructura de formato admite características especiales, como las relaciones de aspecto entrelazadas de vídeo e imagen.

Tanto VMR-7 como VMR-9 admiten [**VIDEOINFOHEADER2 directamente.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Al conectar el VMR al descodificador, negociarán el mejor formato. Sin embargo, el filtro de representador de vídeo anterior no admite **VIDEOINFOHEADER2.** Para usar **los tipos de formato VIDEOINFOHEADER2** con el filtro Representador de vídeo, debe insertar el filtro Overlay [Mixer](overlay-mixer-filter.md) en el gráfico.

1.  Enumere los tipos de medios preferidos en el pin de salida del filtro de descodificador mediante el [**método IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)
2.  Compruebe el primer tipo de medio en la secuencia de enumeración.
3.  Si el tipo de formato es **FORMAT \_ VideoInfo2,** conecte la patilla de salida a la Mixer. A continuación, conecte el Mixer de superposición al representador de vídeo. (Vea [Anclar puertos de](video-port-pins.md)vídeo).

Si no le importan estas características, no tiene que usar el cuadro de Mixer. Conectar el descodificador directamente al representador de vídeo y, en su lugar, se conectará con un [**formato VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Uso de la superposición Mixer captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



