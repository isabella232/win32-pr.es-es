---
description: Establece el modo de procesamiento del Video Stabilization MFT.
ms.assetid: 0D49892A-8628-4F2B-B41B-51160A19DC9B
title: MF_VIDEODSP_MODE atributo (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88383e6bdd197e4912c660657eefa6b9e812fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154973"
---
# <a name="mf_videodsp_mode-attribute"></a>\_Atributo de \_ modo MF VIDEODSP

Establece el modo de procesamiento del [**video stabilization MFT**](video-stabilization-mft.md).

## <a name="data-type"></a>Tipo de datos

**MFVideoDSPMode** almacenado como **UIINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es un valor de enumeración [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) . Este atributo se puede usar para habilitar o deshabilitar la estabilización de la imagen y se puede actualizar para cada ejemplo de salida.

Para establecer este atributo:

1.  Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el MFT de estabilización de vídeo para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para establecer el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Video Stabilization MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




