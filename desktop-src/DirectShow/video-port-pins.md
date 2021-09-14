---
description: Patillas de puerto de vídeo
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: Patillas de puerto de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272916"
---
# <a name="video-port-pins"></a>Patillas de puerto de vídeo

Un dispositivo de captura con un puerto de vídeo de hardware podría usar las extensiones de puerto de vídeo (VPE) en Microsoft® DirectX®. Si es así, el filtro de captura tendrá un pin de puerto de vídeo (VP). Ningún dato de vídeo viaja desde el pin de VP a través del gráfico de filtro. En su lugar, los fotogramas de vídeo se generan en hardware y se envían directamente a la memoria de vídeo. El pin de VP permite enviar mensajes de control al hardware.

Es importante conectar el pin de VP, incluso si la aplicación solo realiza la captura de archivos sin vista previa. Si deja el pin sin conectar, el gráfico no se ejecutará correctamente. Esto es diferente de los pins de vista previa, que no tienen que estar conectados.

Los distintos DirectShow representadores de vídeo proporcionan una compatibilidad variable con los pins de VP:

-   Representador de vídeo: Conectar el pin de VP para anclar 0 en el filtro [Overlay Mixer](overlay-mixer-filter.md) y conecte el filtro Overlay Mixer al representador de vídeo.
-   VMR-7: Conectar el pin de VP al filtro [Administrador](video-port-manager.md) de puertos de vídeo y conecte el Administrador de puertos de vídeo a VMR-7.
-   VMR-9: no se puede usar VMR-9 si el dispositivo tiene un pin de VP, porque Direct3D 9 no admite puertos de vídeo. Use el representador de vídeo o VMR-7.

En escenarios de puerto de vídeo, se recomienda superponer Mixer y Representador de vídeo sobre el Administrador de puertos de vídeo y VMR-7, ya que no todos los controladores admiten el Administrador de puertos de vídeo. En general, la opción Overlay Mixer es la opción más confiable para los puertos de vídeo.

El [**método ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserta automáticamente la propiedad Overlay Mixer si hay un pin de VP. Si va a compilar el gráfico sin usar este método, debe comprobar si hay un pin de puerto de vídeo en el filtro de captura y, si hay alguno, conectarlo al filtro Overlay Mixer, como se muestra en el diagrama siguiente.

![conectar un pin de puerto de vídeo al filtro mezclador superpuesto.](images/vidcap11.png)

Puede usar el método [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para buscar un pin de VP en el filtro de captura:


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



Después de agregar el Mixer superposición al gráfico, vuelva a llamar a **FindPin** para buscar el pin 0 en el cuadro de Mixer. El pin 0 siempre es el primer pin de entrada en el filtro.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Conectar los dos pines llamando a [**IGraphBuilder::Conectar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).


```C++
pGraph->Connect(pVPPin, pOvPin);
```



A continuación, conecte la Mixer de salida de overlay al filtro Video Renderer (Representador de vídeo). Puede ocultar el vídeo llamando a los métodos [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) e [**IVideoWindow::p ut \_ Visible**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) en el Administrador de Graph filtros.

En el caso de los canales de televisión, el filtro de captura también podría tener un pin de VBI del puerto de vídeo (PIN \_ CATEGORY \_ VIDEOPORT \_ VBI). Si es así, conecte ese pin al filtro [De asignador de superficie de VBI.](vbi-surface-allocator.md) Para obtener más información, vea [Ver subtítulos.](viewing-closed-captions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Uso de la función overlay Mixer captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



