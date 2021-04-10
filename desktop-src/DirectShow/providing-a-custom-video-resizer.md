---
description: Proporcionar un tamaño de vídeo personalizado
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Proporcionar un tamaño de vídeo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152198"
---
# <a name="providing-a-custom-video-resizer"></a>Proporcionar un tamaño de vídeo personalizado

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

> [!Note]  
> Esta característica requiere DirectX 9,0 o posterior.

 

Cuando [servicios de edición de DirectShow](directshow-editing-services.md) (des) cambia el tamaño de un clip de origen de vídeo, el comportamiento predeterminado es un *StretchBlt*, que es rápido pero no suavizado. Puede cambiar el comportamiento de cambio de tamaño implementando un ajuste de escala personalizado como filtro de transformación de DirectShow. El filtro debe exponer la interfaz [**IResize**](iresize.md) , que permite a des especificar el tamaño del vídeo de entrada y salida. Para obtener información sobre cómo escribir un filtro de transformación, vea [escribir filtros de transformación](writing-transform-filters.md). La clase base **CTransformFilter** se recomienda como punto de partida. Cuando implemente el filtro, tenga en cuenta lo siguiente:

-   Compatibilidad con la interfaz **IResize** en el filtro (no en los pin).
-   El filtro solo debe aceptar formatos [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (Format \_ info). Rechazar otros tipos de formato.
-   El formato de vídeo de DES puede ser cualquier tipo RGB sin comprimir, incluido RGB de 32 bits con alfa (MEDIASUBTYPE \_ ARGB32). El filtro puede rechazar con seguridad los formatos con **biheight** < 0.
-   Antes de que el motor de representación Conecte el PIN de salida del filtro, llama a [**IResize::p \_**](iresize-put-mediatype.md) el valor de mediatype de UT para establecer el tipo de salida. También puede llamar a [**IResize::p \_ tamaño de UT**](iresize-put-size.md) para ajustar el tamaño de salida. Puede llamar a estos dos métodos en cualquier orden, cualquier número de veces antes de que se conecte el terminal de salida.
-   Una vez que el motor de representación conecta el PIN de salida, podría volver a llamar a **Put \_ size** . El filtro de tamaño debe volver a conectar su PIN de salida con el nuevo tamaño.
-   Dentro del método [**CTransformFilter:: transform**](ctransformfilter-transform.md) del filtro, estire el vídeo de entrada hasta el tamaño de salida.
-   El filtro nunca debe establecer la marca de discontinuidad en el ejemplo de salida o adjuntar un tipo de medio al ejemplo de salida.
-   Para guardar el estado del filtro en un archivo GraphEdit (. GRF), implemente la interfaz **IPersistStream** . (Esto es opcional, pero útil para realizar pruebas).

Para usar el filtro de tamaño, el filtro se debe registrar como un objeto COM en el sistema del usuario. Antes de que la aplicación represente el proyecto de vídeo, consulte el motor de representación de la interfaz [**IRenderEngine2**](irenderengine2.md) y llame a [**IRenderEngine2:: SETRESIZERGUID**](irenderengine2-setresizerguid.md) con el CLSID del filtro de tamaño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar un proyecto](rendering-a-project.md)
</dt> </dl>

 

 



