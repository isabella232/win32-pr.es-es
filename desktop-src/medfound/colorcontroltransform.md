---
description: Ajusta las características de color de una secuencia de vídeo.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: DSP de transformación de control de color (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c51321a8ffd725306f570619b9bcbe70fe7160e784358ce265157145b40347e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606215"
---
# <a name="color-control-transform-dsp"></a>DSP de transformación de control de color

Ajusta las características de color de una secuencia de vídeo.

## <a name="clsid"></a>CLSID

CLSID \_ CColorControlDmo

## <a name="interfaces"></a>Interfaces

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

## <a name="formats"></a>Formatos

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   UYVY
-   YUY2
-   YV12

## <a name="properties"></a>Propiedades

-   [BRILLO DE COLOR DE MFPKEY \_ \_](mfpkey-color-brightness.md)
-   [CONTRASTE DE COLOR MFPKEY \_ \_](mfpkey-color-contrast.md)
-   [MATIZ DE COLOR MFPKEY \_ \_](mfpkey-color-hue.md)
-   [SATURACIÓN DE COLOR MFPKEY \_ \_](mfpkey-color-saturation.md)

## <a name="remarks"></a>Comentarios

Este DSP modifica el contenido de la secuencia de vídeo. Para la reproducción, es posible que pueda lograr efectos similares de forma más eficaz mediante el uso de la interfaz **IMFVideoProcessor,** que controla el procesamiento de vídeo en la tarjeta gráfica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




