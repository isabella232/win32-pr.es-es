---
description: Cambia el tamaño de una secuencia de vídeo.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Tamaño DSP de vídeo (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696672"
---
# <a name="video-resizer-dsp"></a>Vídeo de tamaño DSP

Cambia el tamaño de una secuencia de vídeo.

## <a name="clsid"></a>CLSID

CLSID \_ CResizerDMO

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResizerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a>Formatos

El DSP de tamaño de vídeo admite los siguientes subtipos de medios de entrada/salida cuando actúa como un objeto multimedia de DirectX (DMO).

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ i420
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ AYUV
-   MEDIASUBTYPE \_ V216
-   MEDIASUBTYPE \_ YV12

El DSP de tamaño de vídeo admite los siguientes subtipos de medios de entrada/salida cuando actúa como una transformación de Media Foundation (MFT).

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ i420
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ AYUV
-   MFVideoFormat \_ V216
-   MFVideoFormat \_ YV12

## <a name="properties"></a>Propiedades

-   [MFPKEY \_ cambiar el tamaño de \_ src \_ left](mfpkey-resize-src-left.md)
-   [MFPKEY \_ cambiar tamaño \_ src \_ superior](mfpkey-resize-src-top.md)
-   [MFPKEY \_ cambiar el tamaño de \_ src \_](mfpkey-resize-src-width.md)
-   [MFPKEY \_ cambiar el tamaño de \_ src \_](mfpkey-resize-src-height.md)
-   [MFPKEY \_ cambio de tamaño de DST a la \_ \_ izquierda](mfpkey-resize-dst-left.md)
-   [MFPKEY \_ cambiar el tamaño de \_ DST \_ superior](mfpkey-resize-dst-top.md)
-   [MFPKEY \_ cambiar el \_ ancho de DST \_](mfpkey-resize-dst-width.md)
-   [MFPKEY \_ cambiar el tamaño de \_ DST \_](mfpkey-resize-dst-height.md)
-   [MFPKEY \_ cambiar el tamaño de la \_ calidad](mfpkey-resize-quality.md)
-   [MFPKEY \_ cambiar el tamaño del \_ entrelazado](mfpkey-resize-interlace.md)
-   [MFPKEY \_ cambiar el tamaño de \_ GEOMAPX](mfpkey-resize-geomapx.md)
-   [MFPKEY \_ cambiar el tamaño de \_ GEOMAPY](mfpkey-resize-geomapy.md)
-   [MFPKEY \_ cambiar el tamaño de \_ GEOMAPWIDTH](mfpkey-resize-geomapwidth.md)
-   [MFPKEY \_ cambiar el tamaño de \_ GEOMAPHEIGHT](mfpkey-resize-geomapheight.md)
-   [MFPKEY \_ cambiar el tamaño de \_ MINAPX](mfpkey-resize-minapx.md)
-   [MFPKEY \_ cambiar el tamaño de \_ MINAPY](mfpkey-resize-minapy.md)
-   [MFPKEY \_ cambiar el tamaño de \_ MINAPWIDTH](mfpkey-resize-minapwidth.md)
-   [MFPKEY \_ cambiar el tamaño de \_ MINAPHEIGHT](mfpkey-resize-minapheight.md)
-   [MFPKEY \_ cambiar el tamaño de \_ PANSCANAPX](mfpkey-resize-panscanapx.md)
-   [MFPKEY \_ cambiar el tamaño de \_ PANSCANAPY](mfpkey-resize-panscanapy.md)
-   [MFPKEY \_ cambiar el tamaño de \_ PANSCANAPWIDTH](mfpkey-resize-panscanapwidth.md)
-   [MFPKEY \_ cambiar el tamaño de \_ PANSCANAPHEIGHT](mfpkey-resize-panscanapheight.md)
-   [MFPKEY \_ PIXELASPECTRATIO](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a>Observaciones

El ajuste de vídeo DSP se implementa como un objeto COM que puede actuar como DMO o MFT. El objeto tiene un identificador de clase único (CLSID) independientemente de si actúa como un DMO o MFT. Para obtener información sobre cuándo un DSP actúa como DMO o MFT, consulte [procesadores de señal digital](windowsmediadigitalsignalprocessors.md).

Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un DSP actúa como DMO o MFT. Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un DSP actúa como DMO o MFT. Para obtener información sobre los GUID que representan subtipos de medios, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

Este DSP puede realizar el recorte y el escalado en la imagen de vídeo. El formato del tipo de salida debe coincidir con el formato del tipo de entrada. El DSP no realiza conversiones de espacio de color.

Antes de establecer el tipo de salida, puede definir cualquiera de las siguientes regiones mediante las propiedades que se muestran en esta tabla.



| Region                   | Propiedades                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rectángulo de origen         | MFPKEY \_ cambiar el tamaño de \_ src \_ left<br/> MFPKEY \_ cambiar tamaño \_ src \_ superior<br/> MFPKEY \_ cambiar el tamaño de \_ src \_<br/> MFPKEY \_ cambiar el tamaño de \_ src \_<br/>            |
| Rectángulo de destino    | MFPKEY \_ cambio de tamaño de DST a la \_ \_ izquierda<br/> MFPKEY \_ cambiar el tamaño de \_ DST \_ superior<br/> MFPKEY \_ cambiar el \_ ancho de DST \_<br/> MFPKEY \_ cambiar el tamaño de \_ DST \_<br/>            |
| Abertura geométrica       | MFPKEY \_ cambiar el tamaño de \_ GEOMAPX<br/> MFPKEY \_ cambiar el tamaño de \_ GEOMAPY<br/> MFPKEY \_ cambiar el tamaño de \_ GEOMAPWIDTH<br/> MFPKEY \_ cambiar el tamaño de \_ GEOMAPHEIGHT<br/>             |
| Apertura de pantalla mínima | MFPKEY \_ cambiar el tamaño de \_ MINAPX<br/> MFPKEY \_ cambiar el tamaño de \_ MINAPY<br/> MFPKEY \_ cambiar el tamaño de \_ MINAPWIDTH<br/> MFPKEY \_ cambiar el tamaño de \_ MINAPHEIGHT<br/>                 |
| Región de Pan/Scan          | MFPKEY \_ cambiar el tamaño de \_ PANSCANAPX<br/> MFPKEY \_ cambiar el tamaño de \_ PANSCANAPY<br/> MFPKEY \_ cambiar el tamaño de \_ PANSCANAPWIDTH<br/> MFPKEY \_ cambiar el tamaño de \_ PANSCANAPHEIGHT<br/> |



 

En cada caso, debe establecer todas las propiedades asociadas para que la configuración surta efecto.

El DSP copia la parte de la imagen de origen definida por el rectángulo de origen y lo estira o comprime en el rectángulo de destino en el búfer de salida. No es necesario que los rectángulos de origen y de destino tengan el mismo tamaño. El tamaño del marco en el tipo de medio de salida debe ser lo suficientemente grande como para contener el rectángulo de destino.

La abertura geométrica, la abertura de pantalla mínima y la región de Pan/Scan no afectan al modo en que el DSP cambia el tamaño del vídeo. Sin embargo, podrían afectar al modo en que el componente de nivel inferior interpreta el fotograma de vídeo. En concreto, el representador de vídeo mejorado (EVR) usa estos valores al calcular la relación de aspecto de la imagen y el área de presentación.

Si usa Media Foundation tipos de medios, puede establecer la abertura geométrica, la abertura de pantalla mínima y las regiones de Pan/Scan directamente en el tipo de medio de salida. De lo contrario, si usa tipos de medios DMO, establézcalo mediante las propiedades.

Para obtener más información, vea los temas siguientes:

-   [**\_ \_ apertura geométrica de MF MT \_**](mf-mt-geometric-aperture-attribute.md)
-   [**\_ \_ apertura mínima de \_ pantalla MF MT \_**](mf-mt-minimum-display-aperture-attribute.md)
-   [**\_apertura de \_ \_ análisis panorámico MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vidreszr.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
