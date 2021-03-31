---
description: Muestra cómo implementar un efecto de vídeo como una transformación de Media Foundation (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: Ejemplo de MFT_Grayscale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155356"
---
# <a name="mft_grayscale-sample"></a>\_Ejemplo de escala de grises de MFT

Muestra cómo implementar un efecto de vídeo como una transformación de Media Foundation (MFT). La MFT de escala de grises convierte vídeo YUV en escala de grises estableciendo los valores de croma del vídeo en neutro. La MFT acepta vídeo sin comprimir en los formatos UYVY, YUY2 o NV12.

## <a name="apis-demonstrated"></a>API mostradas

Este ejemplo muestra las siguientes interfaces de Microsoft Media Foundation:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Uso

El \_ ejemplo de escala de grises de MFT crea un archivo DLL que es un servidor com para la MFT. Antes de usar la MFT, debe registrar el archivo DLL.

Para ver la MFT en uso de escala de grises, ejecute el [ejemplo PlaybackFX](/previous-versions//bb970336(v=vs.85)). También puede usar la herramienta TopoEdit para crear una topología que incluya la MFT de escala de grises. Para obtener más información sobre TopoEdit, consulte [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del vídeo YUV](about-yuv-video.md)
</dt> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[Ejemplo de AudioDelay de MFT \_](mft-audiodelay-sample.md)
</dt> <dt>

[Escribir una MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 
