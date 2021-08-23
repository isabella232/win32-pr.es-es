---
description: Cambia el tamaño de una secuencia de vídeo.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: DSP de Video Resizer (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d26dcc53baf38336656d870acc5583066e0816a0bf963217db1da54513ee18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721325"
---
# <a name="video-resizer-dsp"></a>DSP de cambio de tamaño de vídeo

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

El DSP de Video Resizer admite los siguientes subtipos de medios de entrada/salida cuando actúa como un objeto multimedia DirectX (DMO).

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ AYUV
-   MEDIASUBTYPE \_ V216
-   MEDIASUBTYPE \_ YV12

El DSP de Video Resizer admite los siguientes subtipos de medios de entrada/salida cuando actúa como una Media Foundation transformación (MFT).

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ AYUV
-   MFVideoFormat \_ V216
-   MFVideoFormat \_ YV12

## <a name="properties"></a>Propiedades

-   [MFPKEY \_ RESIZE \_ SRC \_ LEFT](mfpkey-resize-src-left.md)
-   [MFPKEY \_ RESIZE \_ SRC \_ TOP](mfpkey-resize-src-top.md)
-   [MFPKEY \_ RESIZE \_ SRC \_ WIDTH](mfpkey-resize-src-width.md)
-   [MFPKEY \_ RESIZE \_ SRC \_ HEIGHT](mfpkey-resize-src-height.md)
-   [MFPKEY \_ RESIZE \_ DST \_ LEFT](mfpkey-resize-dst-left.md)
-   [MFPKEY \_ RESIZE \_ DST \_ TOP](mfpkey-resize-dst-top.md)
-   [MFPKEY \_ RESIZE \_ DST \_ WIDTH](mfpkey-resize-dst-width.md)
-   [MFPKEY \_ RESIZE \_ DST \_ HEIGHT](mfpkey-resize-dst-height.md)
-   [CALIDAD DE CAMBIO DE TAMAÑO DE MFPKEY \_ \_](mfpkey-resize-quality.md)
-   [MFPKEY \_ RESIZE \_ INTERLACE](mfpkey-resize-interlace.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPX](mfpkey-resize-geomapx.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPY](mfpkey-resize-geomapy.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPWIDTH](mfpkey-resize-geomapwidth.md)
-   [MFPKEY \_ RESIZE \_ GEOMAPHEIGHT](mfpkey-resize-geomapheight.md)
-   [MFPKEY \_ RESIZE \_ MINAPX](mfpkey-resize-minapx.md)
-   [MFPKEY \_ RESIZE \_ MINAPY](mfpkey-resize-minapy.md)
-   [MFPKEY \_ RESIZE \_ MINAPWIDTH](mfpkey-resize-minapwidth.md)
-   [MFPKEY \_ RESIZE \_ MINAPHEIGHT](mfpkey-resize-minapheight.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPX](mfpkey-resize-panscanapx.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPY](mfpkey-resize-panscanapy.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPWIDTH](mfpkey-resize-panscanapwidth.md)
-   [MFPKEY \_ RESIZE \_ PANSCANAPHEIGHT](mfpkey-resize-panscanapheight.md)
-   [MFPKEY \_ PIXELASPECTRATIO](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a>Comentarios

El DSP de Video Resizer se implementa como un objeto COM que puede actuar como DMO o MFT. El objeto tiene un identificador de clase única (CLSID) independientemente de si actúa como DMO o MFT. Para obtener información sobre cuándo un DSP actúa como DMO o MFT, vea [Procesadores de señales digitales](windowsmediadigitalsignalprocessors.md).

Los identificadores únicos globales (GUID) de los subtipos de medios RGB difieren en función de si un DSP actúa como un DMO o un MFT. Los GUID para subtipos multimedia no RGB son los mismos, independientemente de si un DSP actúa como un DMO o un MFT. Para obtener información sobre los GUID que representan subtipos multimedia, vea [GUID de subtipo de vídeo.](video-subtype-guids.md)

Este DSP puede realizar el recorte y el escalado en la imagen de vídeo. El formato del tipo de salida debe coincidir con el formato del tipo de entrada. El DSP no realiza conversiones de espacio de color.

Antes de establecer el tipo de salida, puede definir cualquiera de las siguientes regiones mediante las propiedades enumeradas en esta tabla.



| Region                   | Propiedades                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rectángulo de origen         | MFPKEY \_ RESIZE \_ SRC \_ LEFT<br/> MFPKEY \_ RESIZE \_ SRC \_ TOP<br/> MFPKEY \_ RESIZE \_ SRC \_ WIDTH<br/> MFPKEY \_ RESIZE \_ SRC \_ HEIGHT<br/>            |
| Rectángulo de destino    | MFPKEY \_ RESIZE \_ DST \_ LEFT<br/> MFPKEY \_ RESIZE \_ DST \_ TOP<br/> MFPKEY \_ RESIZE \_ DST \_ WIDTH<br/> MFPKEY \_ RESIZE \_ DST \_ HEIGHT<br/>            |
| Apertura geométrica       | MFPKEY \_ RESIZE \_ GEOMAPX<br/> MFPKEY \_ RESIZE \_ GEOMAPY<br/> MFPKEY \_ RESIZE \_ GEOMAPWIDTH<br/> MFPKEY \_ RESIZE \_ GEOMAPHEIGHT<br/>             |
| Apertura de pantalla mínima | MFPKEY \_ RESIZE \_ MINAPX<br/> MFPKEY \_ RESIZE \_ MINAPY<br/> MFPKEY \_ RESIZE \_ MINAPWIDTH<br/> MFPKEY \_ RESIZE \_ MINAPHEIGHT<br/>                 |
| Región de exploración y panorámica          | MFPKEY \_ RESIZE \_ PANSCANAPX<br/> MFPKEY \_ RESIZE \_ PANSCANAPY<br/> MFPKEY \_ RESIZE \_ PANSCANAPWIDTH<br/> MFPKEY \_ RESIZE \_ PANSCANAPHEIGHT<br/> |



 

En cada caso, debe establecer todas las propiedades asociadas para que la configuración suba efecto.

El DSP copia la parte de la imagen de origen definida por el rectángulo de origen y la extiende o comprime en el rectángulo de destino en el búfer de salida. Los rectángulos de origen y destino no necesitan tener el mismo tamaño. El tamaño del marco en el tipo de medio de salida debe ser lo suficientemente grande como para contener el rectángulo de destino.

La apertura geométrica, la apertura de pantalla mínima y la región de panorámica y examen no afectan al modo en que el DSP cambia el tamaño del vídeo. Sin embargo, pueden afectar a la forma en que el componente de bajada interpreta el fotograma de vídeo. En concreto, el representador de vídeo mejorado (EVR) usa estos valores cuando calcula la relación de aspecto de la imagen y el área de visualización.

Si usa tipos Media Foundation multimedia, puede establecer la apertura geométrica, la apertura de pantalla mínima y las regiones de panorámica y examen directamente en el tipo de medio de salida. De lo contrario, si usa DMO de medios, esta establezca con las propiedades .

Para obtener más información, vea los temas siguientes:

-   [**APERTURA \_ GEOMÉTRICA DE MF MT \_ \_**](mf-mt-geometric-aperture-attribute.md)
-   [**APERTURA \_ DE PANTALLA MÍNIMA \_ DE \_ \_ MF MT**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vidreszr.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Procesadores de señal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
