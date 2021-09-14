---
description: Tipo de formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo de formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272868"
---
# <a name="videoinfo2-format-type"></a>Tipo de formato VideoInfo2

El tipo de medio preferido de un pin de vista previa podría ser un tipo con un [**formato VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Esta estructura de formato admite características especiales, como las relaciones de aspecto entrelazadas de vídeo e imagen.

Tanto VMR-7 como VMR-9 admiten [**VIDEOINFOHEADER2 directamente.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Al conectar el VMR al descodificador, negociarán el mejor formato. Sin embargo, el filtro de representador de vídeo anterior no admite **VIDEOINFOHEADER2.** Para usar **los tipos de formato VIDEOINFOHEADER2** con el filtro Representador de vídeo, debe insertar el filtro Overlay [Mixer](overlay-mixer-filter.md) en el gráfico.

1.  Enumere los tipos de medios preferidos en el pin de salida del filtro de descodificador mediante el [**método IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)
2.  Compruebe el primer tipo de medio en la secuencia de enumeración.
3.  Si el tipo de formato es **FORMAT \_ VideoInfo2,** conecte el pin de salida a la Mixer. A continuación, conecte el Mixer superposición al representador de vídeo. (Vea [Anclar puertos de](video-port-pins.md)vídeo).

Si no le importan estas características, no tiene que usar el cuadro de Mixer. Conectar el descodificador directamente al representador de vídeo y, en su lugar, se conectará con un [**formato VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Uso de la función overlay Mixer captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



