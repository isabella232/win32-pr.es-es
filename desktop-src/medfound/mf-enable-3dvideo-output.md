---
description: Especifica cómo una transformación de Media Foundation (MFT) debe generar una secuencia de vídeo estéreo 3D.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: MF_ENABLE_3DVIDEO_OUTPUT atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127364083"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>Atributo MF \_ ENABLE \_ 3DVIDEO \_ OUTPUT

Especifica cómo una transformación de Media Foundation (MFT) debe generar una secuencia de vídeo estéreo 3D.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor del atributo es miembro de la [**enumeración MF3DVideoOutputType.**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype)

Este atributo solo se aplica si MFT devuelve **TRUE para** el atributo [ \_ MFT SUPPORT \_ 3DVIDEO.](mft-support-3dvideo.md)

Para obtener o establecer este atributo, llame [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global de MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




