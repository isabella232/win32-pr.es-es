---
description: PIN de puerto de vídeo
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: PIN de puerto de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d13ab4ad63995dd38460bf29064035c9c1802dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911053"
---
# <a name="video-port-pins"></a>PIN de puerto de vídeo

Un dispositivo de captura con un puerto de vídeo de hardware podría usar las extensiones de puerto de vídeo (VPE) de Microsoft® DirectX®. Si es así, el filtro de captura tendrá un PIN de puerto de vídeo (VP). No se transmiten datos de vídeo desde el eje VP a través del gráfico de filtro. En su lugar, los fotogramas de vídeo se producen en hardware y se envían directamente a la memoria de vídeo. The VP PIN permite enviar mensajes de control al hardware.

Es importante conectar la VP, incluso si la aplicación solo realiza la captura de archivos sin vista previa. Si deja el PIN sin conexión, el gráfico no se ejecutará correctamente. Esto es diferente de los pin de vista previa, que no tienen que estar conectados.

Los distintos representadores de vídeo de DirectShow proporcionan compatibilidad variable para VP PIN:

-   Representador de vídeo: Conecte el código de la VP al pin 0 en el filtro del [mezclador de superposición](overlay-mixer-filter.md) y conecte el filtro de mezclador superpuesto al representador de vídeo.
-   VMR-7: Conecte el código VP al filtro del [Administrador de puertos de vídeo](video-port-manager.md) y conecte el administrador de puertos de vídeo a VMR-7.
-   VMR-9: no puede usar la VMR-9 Si el dispositivo tiene una VP, porque Direct3D 9 no admite puertos de vídeo. Use el representador de vídeo o VMR-7.

En los escenarios de puerto de vídeo, se recomienda usar el mezclador de superposición y el representador de vídeo en el administrador de puertos de vídeo y VMR-7, ya que no todos los controladores son compatibles con el administrador de puertos de vídeo. En general, el mezclador de superposición es la opción más confiable para los puertos de vídeo.

El método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) inserta automáticamente el mezclador de superposición si hay un código de VP. Si va a compilar el gráfico sin utilizar este método, debe comprobar si hay un PIN de puerto de vídeo en el filtro de captura y, si hay alguno, conéctelo al filtro de mezclador de superposición, como se muestra en el diagrama siguiente.

![conexión de un PIN de puerto de vídeo al filtro de mezclador de superposición.](images/vidcap11.png)

Puede usar el método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para buscar una VP en el filtro de captura:


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



Después de agregar el mezclador de superposición al gráfico, vuelva a llamar a **FindPin** para buscar el pin 0 en el mezclador de superposición. El pin 0 siempre es el primer PIN de entrada del filtro.


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



Conecte los dos PIN llamando a [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect).


```C++
pGraph->Connect(pVPPin, pOvPin);
```



A continuación, conecte el PIN de salida del mezclador de superposición al filtro de representador de vídeo. Puede ocultar el vídeo mediante una llamada a los métodos visibles [**IVideoWindow::p UT \_ Autoshow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) y [**IVideoWindow \_ ::P UT**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible) en Filter Graph Manager.

En el caso de los sintonizadores de TV, el filtro de captura también puede tener un PIN de puerto de vídeo VBI (categoría de PIN de \_ \_ videopuerto \_ VBI). Si es así, conecte ese pin al filtro de [asignador de superficie de VBI](vbi-surface-allocator.md) . Para obtener más información, vea [ver subtítulos cerrados](viewing-closed-captions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> <dt>

[Usar el mezclador de superposición en la captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



