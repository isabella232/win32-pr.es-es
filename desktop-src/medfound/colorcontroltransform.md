---
description: Ajusta las características de color de una secuencia de vídeo.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Transformación de control de color DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808161"
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

-   [\_brillo del color de MFPKEY \_](mfpkey-color-brightness.md)
-   [\_contraste de color de MFPKEY \_](mfpkey-color-contrast.md)
-   [\_matiz de color MFPKEY \_](mfpkey-color-hue.md)
-   [\_saturación de color de MFPKEY \_](mfpkey-color-saturation.md)

## <a name="remarks"></a>Observaciones

Este DSP modifica el contenido de la secuencia de vídeo. Para la reproducción, es posible que pueda conseguir efectos similares de forma más eficaz mediante la interfaz **IMFVideoProcessor** , que controla el procesamiento de vídeo en la tarjeta gráfica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




