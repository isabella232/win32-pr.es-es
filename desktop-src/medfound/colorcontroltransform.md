---
description: Ajusta las características de color de una secuencia de vídeo.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: DSP de transformación de control de color (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257959"
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

-   [BRILLO DE COLOR MFPKEY \_ \_](mfpkey-color-brightness.md)
-   [CONTRASTE DE COLOR MFPKEY \_ \_](mfpkey-color-contrast.md)
-   [MATIZ DE COLOR MFPKEY \_ \_](mfpkey-color-hue.md)
-   [SATURACIÓN DE COLOR MFPKEY \_ \_](mfpkey-color-saturation.md)

## <a name="remarks"></a>Observaciones

Este DSP modifica el contenido de la secuencia de vídeo. Para la reproducción, es posible que pueda lograr efectos similares de forma más eficaz mediante la interfaz **DEDEVIDEOVideoProcessor,** que controla el procesamiento de vídeo en la tarjeta gráfica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




