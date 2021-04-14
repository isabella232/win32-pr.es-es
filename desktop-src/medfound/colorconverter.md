---
description: Convierte un flujo de vídeo entre formatos de color.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Convertidor de colores DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496834"
---
# <a name="color-converter-dsp"></a>DSP de convertidor de colores

Convierte un flujo de vídeo entre formatos de color.

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
-   [MFPKEY \_ ancho de COLORCONV \_](mfpkey-colorconv-width.md)
-   [alto de MFPKEY \_ COLORCONV \_](mfpkey-colorconv-height.md)
-   [\_modo COLORCONV de MFPKEY \_](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Observaciones

El DSP del convertidor de colores se implementa como un objeto COM que puede actuar como un objeto DirectXMedia (DMO) o una transformación Media Foundation (MFT). El objeto tiene un identificador de clase único (CLSID) independientemente de si actúa como un DMO o MFT. Para obtener información sobre cuándo un DSP actúa como DMO o MFT, consulte [procesadores de señal digital](windowsmediadigitalsignalprocessors.md).

Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un DSP actúa como DMO o MFT. Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un DSP actúa como DMO o MFT. Para obtener información sobre los GUID que representan subtipos de medios, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

De forma predeterminada, este DSP copia toda la imagen de origen en el búfer de salida. Opcionalmente, puede especificar los rectángulos de origen y de destino. El DSP copia la parte de la imagen de origen definida por el rectángulo de origen y la escribe en el rectángulo de destino en el búfer de salida. El DSP no realiza ningún ajuste de escala; los rectángulos de origen y de destino deben tener el mismo tamaño. Los rectángulos de origen y de destino no pueden superar los límites del fotograma de vídeo.

Todas las propiedades excepto el [**\_ \_ modo MFPKEY COLORCONV**](mfpkey-colorconv-mode.md) se deben establecer en un grupo. Si establece cualquiera de estas propiedades, debe establecer todas las demás. De lo contrario, los rectángulos de origen y de destino podrían no ser válidos, en cuyo caso los métodos [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) y [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) devolverán **E \_ INVALIDARG**.

El convertidor de colores no admite todas las combinaciones de formato de entrada y de salida. Normalmente, debe establecer el formato multimedia que conoce, ya sea de entrada o de salida, y, a continuación, enumerar los formatos disponibles en la secuencia opuesta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
