---
description: Usar el mezclador de superposición en la captura de vídeo
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Usar el mezclador de superposición en la captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082949"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>Usar el mezclador de superposición en la captura de vídeo

Hay determinados tipos de vídeo que el filtro de [representador de vídeo](video-renderer-filter.md) no puede mostrar por sí mismo. En estas situaciones, el representador de vídeo debe trabajar con el filtro de [mezclador de superposición](overlay-mixer-filter.md) . El mezclador de superposición administra la representación, mientras que el representador de vídeo administra la ventana de vídeo. El mezclador de superposición es necesario en las situaciones siguientes:

-   Clavijas del puerto de vídeo (VP). Si el dispositivo de captura usa un puerto de vídeo, el mezclador de superposición administra la superposición de hardware.
-   Vídeo entrelazado. En el caso del vídeo entrelazado, el descodificador requiere un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , que no es compatible con el representador de vídeo.
-   Subtítulos (CC). El texto de la leyenda se representa como mapa de bits de 8 bits por píxel, que el mezclador de superposición se superpone en el vídeo.

El método **RenderStream** del generador de gráficos de captura inserta el mezclador de superposición siempre que sea necesario. Sin embargo, si va a compilar el gráfico sin usar el generador de gráficos de captura, debe comprobar cada una de estas situaciones e insertar el mezclador de superposición usted mismo.

-   \[! Aún\]  
    > Si el dispositivo tiene una VP, debe conectar el mezclador de superposición, incluso si no necesita la funcionalidad de versión preliminar en la aplicación. Con un puerto de vídeo, el dispositivo de captura siempre envía los datos de vídeo a la superposición de hardware, por lo que siempre es necesario el mezclador de superposición.

     

Los filtros de representador de combinación de vídeo (VMR-7 y VMR-9) admiten vídeo entrelazado y pueden mezclar mapas de bits de subtítulos cerrados en el vídeo principal. Si usa la VMR para esos escenarios, no es necesario usar el mezclador de superposición. VMR-9 no es compatible con las conexiones de VP PIN. VMR-7 admite las conexiones de VP PIN a través del filtro del administrador de puertos de vídeo. Sin embargo, es posible que algunos controladores no funcionen correctamente con el administrador de puertos de vídeo. Por ese motivo, todavía se recomienda usar el mezclador de superposición para VICEPRESIDENTEs.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[PIN de puerto de vídeo](video-port-pins.md)
</dt> <dt>

[Tipo de formato VideoInfo2](videoinfo2-format-type.md)
</dt> </dl>

 

 



