---
description: Cambia la velocidad de fotogramas de una secuencia de vídeo.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: Convertidor de velocidad de fotogramas DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6197c29e9e753db6f327aa8b2797ba04131448d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808072"
---
# <a name="frame-rate-converter-dsp"></a>DSP de convertidor de velocidad de fotogramas

Cambia la velocidad de fotogramas de una secuencia de vídeo.

## <a name="clsid"></a>CLSID

CLSID \_ CFrameRateConvertDmo

## <a name="interfaces"></a>Interfaces

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

## <a name="formats"></a>Formatos

-   ARGB 32
-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   IYUV
-   UYVY
-   Y211
-   Y411
-   Y41P
-   YUY2
-   YUYV
-   YV12
-   YVYU

## <a name="properties"></a>Propiedades

-   [MFPKEY \_ conv \_ INPUTFRAMERATE](mfpkey-conv-inputframerate.md)
-   [MFPKEY \_ conv \_ OUTPUTFRAMERATE](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Observaciones

Este DSP cambia la velocidad de fotogramas repitiendo o colocando fotogramas.

De forma predeterminada, el DSP obtiene las velocidades de fotogramas de los tipos de medios. Opcionalmente, puede especificar las velocidades de fotogramas mediante el establecimiento de las \_ propiedades MFPKEY CONV \_ INPUTFRAMERATE y MFPKEY \_ conv \_ OUTPUTFRAMERATE. Estos valores invalidan la velocidad de fotogramas proporcionada en el tipo de medio. Sin embargo, si usa este DSP dentro de la canalización de Media Foundation, no debe establecer estas propiedades.

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

 

 




