---
description: Proporcionar un cambio de tamaño de vídeo personalizado
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Proporcionar un cambio de tamaño de vídeo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160116"
---
# <a name="providing-a-custom-video-resizer"></a>Proporcionar un cambio de tamaño de vídeo personalizado

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

> [!Note]  
> Esta característica requiere DirectX 9.0 o posterior.

 

Cuando [DirectShow Editing Services](directshow-editing-services.md) (DES) cambia el tamaño de un clip de origen de vídeo, el comportamiento predeterminado es *StretchBlt,* que es rápido pero no suavizado de alias. Puede cambiar el comportamiento de cambio de tamaño implementando un cambio de tamaño personalizado como filtro DirectShow transformación. El filtro debe exponer la [**interfaz IResize,**](iresize.md) que permite a DES especificar el tamaño del vídeo de entrada y salida. Para obtener información sobre cómo escribir un filtro de transformación, vea [Escribir filtros de transformación.](writing-transform-filters.md) La clase base **CTransformFilter** se recomienda como punto de partida. Al implementar el filtro, tenga en cuenta lo siguiente:

-   Admite la **interfaz IResize** en el filtro (no en los pines).
-   El filtro solo debe aceptar [**formatos VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (FORMAT \_ VideoInfo). Rechazar otros tipos de formato.
-   El formato de vídeo de DES puede ser cualquier tipo RGB sin comprimir, incluido RGB de 32 bits con alfa (MEDIASUBTYPE \_ ARGB32). El filtro puede rechazar de forma segura los formatos **con biHeight** < 0.
-   Antes de que el motor de representación conecte el pin de salida del filtro, llama a [**IResize::p ut \_ MediaType para**](iresize-put-mediatype.md) establecer el tipo de salida. También puede llamar a [**IResize::p ut \_ Size**](iresize-put-size.md) para ajustar el tamaño de salida. Puede llamar a estos dos métodos en cualquier orden, cualquier número de veces, antes de conectar el pin de salida.
-   Después de que el motor de representación conecte el pin de salida, podría llamar a **put \_ Size de** nuevo. El filtro de cambio de tamaño debe volver a conectar su pin de salida con el nuevo tamaño.
-   Dentro del método [**CTransformFilter::Transform**](ctransformfilter-transform.md) del filtro, estrese el vídeo de entrada al tamaño de salida.
-   El filtro nunca debe establecer la marca de discontinuidad en el ejemplo de salida ni adjuntar un tipo de medio al ejemplo de salida.
-   Para guardar el estado del filtro en un archivo GraphEdit (.grf), implemente la **interfaz IPersistStream.** (Esto es opcional, pero útil para las pruebas).

Para usar el filtro de cambio de tamaño, el filtro debe registrarse como un objeto COM en el sistema del usuario. Antes de que la aplicación represente el proyecto de vídeo, consulte el motor de representación de la interfaz [**IRenderEngine2**](irenderengine2.md) y llame a [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) con el CLSID del filtro de cambio de tamaño.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representación de un Project](rendering-a-project.md)
</dt> </dl>

 

 



