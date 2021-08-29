---
description: Muestra cómo implementar un efecto de vídeo como una transformación Media Foundation (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: MFT_Grayscale ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff29705476869b25aeb42157ebe4878131397988cc56eccc842fcb81134fb8db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102175"
---
# <a name="mft_grayscale-sample"></a>Ejemplo de escala \_ de grises de MFT

Muestra cómo implementar un efecto de vídeo como una transformación Media Foundation (MFT). El MFT de escala de grises convierte el vídeo de YUV a escala de grises estableciendo los valores de los colores del vídeo en neutros. MFT acepta vídeo sin comprimir en formatos UYVY, YUY2 o NV12.

## <a name="apis-demonstrated"></a>API demostradas

En este ejemplo se muestran las interfaces Microsoft Media Foundation siguientes:

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Uso

El ejemplo de Escala de grises de MFT \_ compila un archivo DLL que es un servidor COM para MFT. Antes de usar MFT, debe registrar el archivo DLL.

Para ver el MFT de escala de grises en uso, ejecute [el ejemplo playbackFX](/previous-versions//bb970336(v=vs.85)). También puede usar la herramienta TopoEdit para crear una topología que incluya el MFT de escala de grises. Para obtener más información sobre TopoEdit, vea [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Producto                                                        | Versión   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Este ejemplo está disponible en el repositorio [de github Windows ejemplos clásicos](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de YUV Video](about-yuv-video.md)
</dt> <dt>

[Muestras de SDK de Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> <dt>

[Ejemplo de \_ AudioDelay de MFT](mft-audiodelay-sample.md)
</dt> <dt>

[Escritura de un MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 
