---
description: Uso de la función overlay Mixer captura de vídeo
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Uso de la función overlay Mixer captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891548"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>Uso de la función overlay Mixer captura de vídeo

Hay ciertos tipos de vídeo que el filtro [Representador de](video-renderer-filter.md) vídeo no puede mostrar por sí solo. En estas situaciones, el representador de vídeo debe trabajar con el filtro [overlay Mixer.](overlay-mixer-filter.md) El objeto Overlay Mixer la representación, mientras que el representador de vídeo administra la ventana de vídeo. La superposición Mixer se necesita en las situaciones siguientes:

-   Patillas de puerto de vídeo (VP). Si el dispositivo de captura usa un puerto de vídeo, el Mixer la superposición de hardware.
-   Vídeo entrelazado. En el caso del vídeo entrelazado, el descodificador requiere un formato [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) que el representador de vídeo no admite.
-   Subtítulos. El texto del título se representa como mapas de bits de 8 bits por píxel, que la superposición Mixer superpone en el vídeo.

El método **RenderStream** de Capture Graph Builder inserta el objeto Overlay Mixer sea necesario. Sin embargo, si va a compilar el gráfico sin usar Capture Graph Builder, debe comprobar cada una de estas situaciones e insertar la superposición Mixer usted mismo.

-   \[! Importante\]  
    > Si el dispositivo tiene un pin de VP, debe conectar el dispositivo de superposición Mixer incluso si no necesita la funcionalidad de vista previa en la aplicación. Con un puerto de vídeo, el dispositivo de captura siempre envía los datos de vídeo a la superposición de hardware, por lo que siempre se necesita el Mixer superposición.

     

Los filtros de representador de mezcla de vídeo (VMR-7 y VMR-9) admiten vídeo entrelazado y pueden mezclar mapas de bits de subtítulos en el vídeo principal. Si usa vmr para esos escenarios, no es necesario usar el cuadro de Mixer. VMR-9 no admite conexiones de pin de VP. VMR-7 admite conexiones de pin de VP a través del filtro Administrador de puertos de vídeo. Sin embargo, es posible que algunos controladores no funcionen correctamente con el Administrador de puertos de vídeo. Por ese motivo, se sigue Mixer de superposición para los pins de VP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Anclar puertos de vídeo](video-port-pins.md)
</dt> <dt>

[Tipo de formato VideoInfo2](videoinfo2-format-type.md)
</dt> </dl>

 

 



