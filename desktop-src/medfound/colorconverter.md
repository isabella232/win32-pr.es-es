---
description: Convierte una secuencia de vídeo entre formatos de color.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: DSP del convertidor de colores (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e97db9f3131ed7cea9076255005149544363ba8d6b548736a211973cda3999d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880667"
---
# <a name="color-converter-dsp"></a>DSP de convertidor de colores

Convierte una secuencia de vídeo entre formatos de color.

## <a name="clsid"></a>CLSID

CLSID \_ CColorConvertDMO

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [IWMColorConvProps](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a>Formatos de entrada

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   Y41P
-   Y41T
-   Y42T
-   YUY2
-   YV12
-   YVU9
-   YVYU

## <a name="output-formats"></a>Formatos de salida

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   YUY2
-   YV12
-   YVYU

## <a name="properties"></a>Propiedades

-   [MFPKEY \_ COLORCONV \_ SRCLEFT](mfpkey-colorconv-srcleft.md)
-   [MFPKEY \_ COLORCONV \_ SRCTOP](mfpkey-colorconv-srctop.md)
-   [MFPKEY \_ COLORCONV \_ DSTLEFT](mfpkey-colorconv-dstleft.md)
-   [MFPKEY \_ COLORCONV \_ DSTTOP](mfpkey-colorconv-dsttop.md)
-   [MFPKEY \_ COLORCONV \_ WIDTH](mfpkey-colorconv-width.md)
-   [MFPKEY \_ COLORCONV \_ HEIGHT](mfpkey-colorconv-height.md)
-   [MFPKEY \_ COLORCONV \_ MODE](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Comentarios

El DSP del convertidor de colores se implementa como un objeto COM que puede actuar como un objeto DirectXMedia (DMO) o una transformación de Media Foundation (MFT). El objeto tiene un identificador de clase única (CLSID) independientemente de si actúa como un DMO o un MFT. Para obtener información sobre cuándo un DSP actúa como un DMO o un MFT, vea [Procesadores de señal digital](windowsmediadigitalsignalprocessors.md).

Los identificadores únicos globales (GUID) de los subtipos de medios RGB difieren en función de si un DSP actúa como un DMO o un MFT. Los GUID de los subtipos multimedia no RGB son los mismos, independientemente de si un DSP actúa como un DMO o un MFT. Para obtener información sobre los GUID que representan subtipos multimedia, vea [GUID de subtipo de vídeo.](video-subtype-guids.md)

De forma predeterminada, este DSP copia toda la imagen de origen en el búfer de salida. Opcionalmente, puede especificar rectángulos de origen y destino. El DSP copia la parte de la imagen de origen definida por el rectángulo de origen y la escribe en el rectángulo de destino en el búfer de salida. El DSP no realiza ningún escalado; los rectángulos de origen y destino deben tener el mismo tamaño. Los rectángulos de origen y destino no pueden superar los límites del fotograma de vídeo.

Todas las propiedades excepto [**MFPKEY \_ COLORCONV \_ MODE**](mfpkey-colorconv-mode.md) deben establecerse en un grupo. Si establece cualquiera de estas propiedades, debe establecer todas las demás. De lo contrario, los rectángulos de origen y destino podrían no ser válidos, en cuyo caso los métodos [**ODBCTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) e [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) **devolverán E \_ INVALIDARG**.

El convertidor de colores no admite todas las combinaciones de formato de entrada y formato de salida. Normalmente, debe establecer el formato multimedia que conoce, ya sea entrada o salida, y, a continuación, enumerar los formatos disponibles en la secuencia opuesta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
