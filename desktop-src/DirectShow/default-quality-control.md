---
description: Control de calidad predeterminado
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Control de calidad predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df737855376db52a35476c0f01da4b850e3678ec20595ee82720b7b928237ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953143"
---
# <a name="default-quality-control"></a>Control de calidad predeterminado

Las [DirectShow base implementan](directshow-base-classes.md) algunos comportamientos predeterminados para el control de calidad del vídeo.

Los mensajes de calidad comienzan en el representador. La clase base para los representadores de vídeo [**es CBaseVideoRenderer,**](cbasevideorenderer.md)que tiene el comportamiento siguiente:

1.  Cuando el representador de vídeo recibe un ejemplo, compara la marca de tiempo de la muestra con la hora de referencia actual.
2.  El representador de vídeo genera un mensaje de calidad. En la clase base, el miembro **Proportion** del mensaje de calidad se limita a un intervalo de 500 (50 %) a 2000 (200 %). Los valores fuera de este intervalo podrían producir cambios bruscos de calidad.
3.  De forma predeterminada, el representador de vídeo envía el mensaje de calidad al pin de salida ascendente (el pin conectado a su pin de entrada). Las aplicaciones pueden invalidar este comportamiento llamando al **método SetSink.**

Lo que sucede a continuación depende del filtro ascendente. Normalmente, se trata de un filtro de transformación. La clase base para los filtros de transformación es [**CTransformFilter**](ctransformfilter.md), que usa las clases [**CTransformInputPin**](ctransforminputpin.md) y [**CTransformOutputPin**](ctransformoutputpin.md) para implementar los pines de entrada y salida. Juntas, estas clases tienen el comportamiento siguiente:

1.  El [**método CTransformOutputPin::Notify**](ctransformoutputpin-notify.md) llama a [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md), un método privado en la clase base de filtro.
2.  Los filtros derivados pueden **invalidar AlterQuality para** controlar el mensaje de calidad. De forma predeterminada, **AlterQuality** omite el mensaje de calidad.
3.  Si **AlterQuality** no controla el mensaje de calidad, el pin de salida llama a [**CBaseInputPin::P assNotify**](cbaseinputpin-passnotify.md), un método privado en el pin de entrada del filtro.
4.  **PassNotify pasa** el mensaje de calidad al lugar adecuado: el siguiente pin de salida ascendente o un administrador de calidad personalizado.

Suponiendo que ningún filtro de transformación controla el mensaje de calidad, el mensaje llega finalmente al pin de salida en el filtro de origen. En las clases base, [**CBasePin::Notify**](cbasepin-notify.md) devuelve E \_ NOTIMPL. La forma en que un filtro de origen determinado controla los mensajes de calidad depende de la naturaleza del origen. Algunos orígenes, como la captura de vídeo en directo, no pueden realizar un control de calidad significativo. Otros orígenes pueden ajustar la velocidad a la que entregan ejemplos.

En el diagrama siguiente se muestra el comportamiento predeterminado.

![control de calidad en las clases base](images/quality-control.png)

El representador de vídeo base implementa **IQualityControl::Notify**, lo que significa que puede pasar mensajes de calidad al propio representador. Si establece el miembro **Proporción** en un valor menor que 1000, el representador de vídeo inserta un período de espera entre cada fotograma que representa, lo que ralentiza el representador. (Por ejemplo, puede hacerlo para reducir el uso del sistema). Para obtener más información, [**vea CBaseVideoRenderer::ThrottleWait**](cbasevideorenderer-throttlewait.md). Establecer el **miembro Proportion** en un valor mayor que 1000 no tiene ningún efecto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de control de calidad](quality-control-management.md)
</dt> </dl>

 

 



