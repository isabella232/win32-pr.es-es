---
title: Información general sobre recursos
description: Describe los recursos de Direct2D y cómo se pueden compartir.
ms.assetid: afd308a7-9524-4436-9a0e-8575383d96fa
keywords:
- Direct2D, recursos
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bf4eb807a25b592e32a2d83436532af17462d70c
ms.sourcegitcommit: 7d0cc7eb398fee8f5be55cd654a12d29937d643c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2021
ms.locfileid: "104361799"
---
# <a name="resources-overview"></a>Información general sobre recursos

Un recurso de Direct2D es un objeto que se usa para dibujar y se representa mediante una interfaz de Direct2D, como [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) o [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). En este tema se describen los tipos de recursos de Direct2D y cómo se pueden compartir.

Este tema contiene las siguientes secciones:

-   [Acerca de los recursos de Direct2D](#about-direct2d-resources)
-   [Recursos independientes del dispositivo](#device-independent-resources)
-   [Recursos dependientes del dispositivo](#device-dependent-resources)
-   [Compartir recursos de fábrica](#sharing-factory-resources)
-   [Compartir recursos de destino de representación](#sharing-render-target-resources)
    -   [Objetivos de representación de hardware](#hardware-render-targets)
    -   [Objetivos de representación de la superficie de DXGI](#dxgi-surface-render-targets)
    -   [Destinos de representación compatibles y mapas de bits compartidos](#compatible-render-targets-and-shared-bitmaps)

## <a name="about-direct2d-resources"></a>Acerca de los recursos de Direct2D

Muchas API de 2D con aceleración de hardware están diseñadas en torno a un modelo de recursos centrado en la CPU y un conjunto de operaciones de representación que funcionan bien en las CPU. a continuación, parte de la API es acelerada por hardware. La implementación de estas API requiere un administrador de recursos para asignar recursos de CPU a los recursos de la GPU. Debido a las limitaciones de la GPU, es posible que algunas operaciones no se puedan acelerar en todas las circunstancias. En estos casos, el administrador de recursos debe comunicarse entre la CPU y la GPU (que es caro) para que pueda realizar la transición a la representación de la CPU. En algunos casos, podría forzar la representación de forma imprevisible para revertir completamente a la CPU. Además, las operaciones de representación que parecen simples pueden requerir pasos de representación intermedios temporales que no se exponen en la API y que requieren recursos de GPU adicionales.

Direct2D proporciona una asignación más directa para hacer un uso completo de la GPU. Proporciona dos categorías de recursos: independiente del dispositivo y dependiente del dispositivo.

-   Los recursos independientes del dispositivo, como [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), se mantienen en la CPU.
-   Los recursos dependientes del dispositivo, como [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) y [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), se asignan directamente a los recursos de la GPU (cuando la aceleración de hardware está disponible). Las llamadas de representación se realizan mediante la combinación de información de vértices y de cobertura de una geometría con información de texturas generada por los recursos dependientes del dispositivo.

Al crear recursos dependientes del dispositivo, los recursos del sistema (la GPU, si está disponible o la CPU) se asignan cuando se crea el dispositivo y no cambian de una operación de representación a otra. Esta situación elimina la necesidad de un administrador de recursos. Además de las mejoras de rendimiento generales que proporciona la eliminación de un administrador de recursos, este modelo permite controlar directamente cualquier representación intermedia.

Dado que Direct2D proporciona tanto control sobre los recursos, debe comprender los diferentes tipos de recursos y cuándo se pueden usar juntos.

## <a name="device-independent-resources"></a>Recursos de Device-Independent

Tal y como se describe en la sección anterior, los recursos independientes del dispositivo siempre residen en la CPU y nunca se asocian a un dispositivo de representación de hardware. Los siguientes son recursos independientes del dispositivo:

-   [**ID2D1DrawingStateBlock**](/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock)
-   [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
-   [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) y las interfaces que heredan de él.
-   [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) y [ **ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)
-   [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle)

Use un [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), a su vez, un recurso independiente del dispositivo, para crear recursos independientes del dispositivo. (Para crear un generador, use la función [**CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) ).

Excepto en el caso de los destinos de representación, todos los recursos creados por una fábrica son independientes del dispositivo. Un destino de representación es un recurso dependiente del dispositivo.

## <a name="device-dependent-resources"></a>Recursos de Device-Dependent

Cualquier recurso que no se denomine en la lista anterior es un recurso dependiente del dispositivo. Los recursos dependientes del dispositivo se asocian a un dispositivo de representación determinado. Cuando la aceleración de hardware está disponible, el dispositivo es la GPU. En otros casos, es la CPU.

Para crear la mayoría de los recursos dependientes del dispositivo, use un destino de representación. En la mayoría de los casos, use un generador para crear un destino de representación.

A continuación se muestran ejemplos de recursos dependientes del dispositivo:

-   [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) y las interfaces que heredan de él. Use un destino de representación para crear pinceles.
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer). Use un destino de representación para crear capas.
-   [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) y las interfaces que heredan de él. Para crear un destino de representación, utilice un generador u otro destino de representación.

> [!Note]  
> A partir de Windows 8, hay nuevas interfaces que crean recursos dependientes del dispositivo. Un [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) y un [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) pueden compartir un recurso si el contexto del dispositivo y el recurso se crean a partir de la misma **ID2D1Device**.

 

Los recursos dependientes del dispositivo se vuelven inutilizables cuando los dispositivos de representación asociados dejan de estar disponibles. Esto significa que, cuando reciba el error de [**\_ \_ destino de recreación de D2DERR**](direct2d-error-codes.md) para un destino de representación, debe volver a crear el destino de representación y todos sus recursos.

## <a name="sharing-factory-resources"></a>Compartir recursos de fábrica

Puede compartir todos los recursos independientes del dispositivo creados por una fábrica con todos los demás recursos (independientes del dispositivo o dependientes del dispositivo) creados por el mismo generador. Por ejemplo, puede usar dos objetos [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) para dibujar el mismo [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) si ambos objetos **ID2D1RenderTarget** fueron creados por el mismo generador.

Las interfaces de receptor ([**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink), [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)y [**ID2D1TessellationSink**](/windows/win32/api/d2d1/nn-d2d1-id2d1tessellationsink)) se pueden compartir con los recursos creados por cualquier factoría. A diferencia de otras interfaces en Direct2D, se puede usar cualquier implementación de una interfaz de receptor. Por ejemplo, podría usar su propia implementación de **ID2D1SimplifiedGeometrySink**.

## <a name="sharing-render-target-resources"></a>Compartir recursos de destino de representación

La capacidad de compartir recursos creados por un destino de representación depende del tipo de destino de representación. Cuando se crea un destino de representación de tipo [**D2D1 \_ Render \_ target \_ Type \_ default**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type), los recursos creados por ese destino de representación solo se pueden usar en ese destino de representación (a menos que el destino de representación quepa en una de las categorías descritas en las secciones siguientes). Esto se debe a que no sabe qué dispositivo terminará con el destino de representación; podría acabar la representación en el hardware local, el software o el hardware de un cliente remoto. Por ejemplo, puede escribir un programa que deje de funcionar cuando se muestre de forma remota o cuando el destino de representación aumente de tamaño más allá del tamaño máximo admitido por el hardware de representación.

En las secciones siguientes se describen las circunstancias en las que un recurso creado por un destino de representación se puede compartir con otro destino de representación.

### <a name="hardware-render-targets"></a>Objetivos de representación de hardware

Puede compartir recursos entre cualquier destino de representación que use el hardware explícitamente, siempre y cuando el modo de comunicación remota sea compatible. Solo se garantiza que el modo de comunicación remota es compatible cuando ambos destinos de representación usan la marca de uso de uso del destino de representación de [**\_ mapa de \_ \_ \_ \_ bits \_ Remoting**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) o de **D2D1 \_ Render \_ \_ \_ \_ target** , o si no se especifica ninguna marca. Esta configuración garantiza que los recursos se encuentren siempre en el mismo equipo. Para especificar un modo de uso, establezca el campo de **uso** de la estructura de propiedades de destino de representación de D2D1 que usó para crear el destino de representación con una o más marcas de **uso de destino de representación de D2D1 \_ \_ \_** . [**\_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)

Para crear un destino de representación que use explícitamente la representación de hardware, establezca el campo de **tipo** de la estructura de propiedades de destino de representación de D2D1 que usó para crear el destino de representación en el [**hardware de \_ \_ \_ tipo \_ de destino**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)de representación D2D1. [**\_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)

### <a name="dxgi-surface-render-targets"></a>Objetivos de representación de la superficie de DXGI

Puede compartir los recursos creados por un destino de representación de la superficie de DXGI con cualquier otro destino de representación de la superficie de DXGI que use el mismo dispositivo Direct3D subyacente.

### <a name="compatible-render-targets-and-shared-bitmaps"></a>Destinos de representación compatibles y mapas de bits compartidos

Puede compartir recursos entre un destino de representación y destinos de representación compatibles creados por ese destino de representación. Para crear un destino de representación compatible, use el método [**ID2D1RenderTarget:: CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) .

Puede usar el método [**ID2D1RenderTarget:: CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) para crear un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) que se puede compartir entre los dos destinos de representación que se especifican en la llamada al método, si el método se ejecuta correctamente. Este método se realizará correctamente siempre y cuando los dos destinos de representación utilicen el mismo dispositivo subyacente para la representación.

 

 
