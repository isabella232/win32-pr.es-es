---
description: Establece el modo de procesamiento del Video Stabilization MFT.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: MF_VIDEODSP_MODE atributo (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29cb1aff27fb0c4077e26ef47b1cb19804e12d968158e39c34a7b3aa131bbe50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955035"
---
# <a name="mf_videodsp_mode-attribute"></a>Atributo \_ MF VIDEODSP \_ MODE

Establece el modo de procesamiento del [**Video Stabilization MFT.**](video-stabilization-mft.md)

## <a name="data-type"></a>Tipo de datos

**MFVideoDSPMode almacenado** como **UIINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un valor [**de enumeración MFVideoDSPMode.**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) Este atributo se puede usar para habilitar o deshabilitar la estabilización de la imagen y se puede actualizar para cada ejemplo de salida.

Para establecer este atributo:

1.  Llame [**a IMFTransform::GetAttributes en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) el MFT de estabilización de vídeo para obtener un puntero [**DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Llame [**aATTRIBUTEAttributes::SetUINT32 para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) establecer el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Video Stabilization MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




