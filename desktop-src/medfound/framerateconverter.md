---
description: Cambia la velocidad de fotogramas de una secuencia de vídeo.
ms.assetid: a66b9c52-a015-41d2-b27a-3ce6a4d95be9
title: DSP del convertidor de velocidad de fotogramas (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca4a728f37caa43ee99a0d293d5113e9c26cfb1dcfe51f399482fb614283737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600495"
---
# <a name="frame-rate-converter-dsp"></a>DSP del convertidor de velocidad de fotogramas

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

-   [\_INPUTFRAMERATE DE MFPKEY CONV \_](mfpkey-conv-inputframerate.md)
-   [MFPKEY \_ CONV \_ OUTPUTFRAMERATE](mfpkey-conv-outputframerate.md)

## <a name="remarks"></a>Comentarios

Este DSP cambia la velocidad de fotogramas repitiendo o quitando fotogramas.

De forma predeterminada, el DSP obtiene las velocidades de fotogramas de los tipos de medios. Opcionalmente, puede especificar las velocidades de fotogramas estableciendo las propiedades \_ \_ INPUTFRAMERATE y MFPKEY \_ CONV \_ OUTPUTFRAMERATE de MFPKEY. Estos valores invalidan la velocidad de fotogramas dada en el tipo de medio. Sin embargo, si usa este DSP dentro de la Media Foundation, no debe establecer estas propiedades.

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

 

 




