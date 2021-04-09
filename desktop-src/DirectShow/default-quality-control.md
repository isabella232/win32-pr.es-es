---
description: Control de calidad predeterminado
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Control de calidad predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864cd187df71c56441edcfd00fcd6785d96afe84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079889"
---
# <a name="default-quality-control"></a>Control de calidad predeterminado

Las [clases base de DirectShow](directshow-base-classes.md) implementan algunos comportamientos predeterminados para el control de calidad de vídeo.

Los mensajes de calidad comienzan en el representador. La clase base para los representadores de vídeo es [**CBaseVideoRenderer**](cbasevideorenderer.md), que tiene el siguiente comportamiento:

1.  Cuando el representador de vídeo recibe un ejemplo, compara la marca de tiempo del ejemplo con el tiempo de referencia actual.
2.  El representador de vídeo genera un mensaje de calidad. En la clase base, el miembro **proporciones** del mensaje de calidad está limitado a un intervalo de 500 (50%). a 2000 (200%). Los valores que se encuentran fuera de este intervalo podrían provocar cambios de calidad bruscos.
3.  De forma predeterminada, el representador de vídeo envía el mensaje de calidad al pin de salida ascendente (el PIN conectado a su clavija de entrada). Las aplicaciones pueden invalidar este comportamiento llamando al método **SetSink** .

Lo que sucede después depende del filtro de nivel superior. Normalmente, se trata de un filtro de transformación. La clase base para los filtros de transformación es [**CTransformFilter**](ctransformfilter.md), que usa las clases [**CTransformInputPin**](ctransforminputpin.md) y [**CTransformOutputPin**](ctransformoutputpin.md) para implementar los terminales de entrada y salida. Juntas, estas clases tienen el siguiente comportamiento:

1.  El método [**CTransformOutputPin:: Notify**](ctransformoutputpin-notify.md) llama a [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md), un método privado en la clase base de filtro.
2.  Los filtros derivados pueden invalidar **AlterQuality** para controlar el mensaje de calidad. De forma predeterminada, **AlterQuality** omite el mensaje de calidad.
3.  Si **AlterQuality** no controla el mensaje de calidad, el PIN de salida llama a [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md), un método privado en el PIN de entrada del filtro.
4.  **PassNotify** pasa el mensaje de calidad al lugar adecuado: el siguiente PIN de salida ascendente o un administrador de calidad personalizado.

Suponiendo que ningún filtro de transformación controle el mensaje de calidad, el mensaje alcanza el PIN de salida en el filtro de origen. En las clases base, [**CBasePin:: Notify**](cbasepin-notify.md) devuelve E \_ NOTIMPL. El modo en que un filtro de origen determinado controla los mensajes de calidad depende de la naturaleza del origen. Algunos orígenes, como la captura de vídeo en directo, no pueden realizar un control de calidad significativo. Otros orígenes pueden ajustar la velocidad a la que proporcionan ejemplos.

En el diagrama siguiente se muestra el comportamiento predeterminado.

![control de calidad en las clases base](images/quality-control.png)

El representador de vídeo básico implementa **IQualityControl:: Notify**, lo que significa que puede pasar mensajes de calidad al propio representador. Si establece el miembro **proporciones** en un valor inferior a 1000, el representador de vídeo inserta un período de espera entre cada fotograma que representa, lo que hace que se ralentice el representador. (Puede hacer esto para reducir el uso del sistema, por ejemplo). Para obtener más información, vea [**CBaseVideoRenderer:: ThrottleWait**](cbasevideorenderer-throttlewait.md). Establecer el miembro de **proporción** en un valor mayor que 1000 no tiene ningún efecto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de control de calidad](quality-control-management.md)
</dt> </dl>

 

 



