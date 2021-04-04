---
description: Especifica cómo una transformación de Media Foundation (MFT) debe generar una secuencia de vídeo Stereoscopic 3D.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: MF_ENABLE_3DVIDEO_OUTPUT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908461"
---
# <a name="mf_enable_3dvideo_output-attribute"></a>MF \_ habilitar \_ atributo de salida de 3DVIDEO \_

Especifica cómo una transformación de Media Foundation (MFT) debe generar una secuencia de vídeo Stereoscopic 3D.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor del atributo es un miembro de la enumeración [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .

Este atributo solo se aplica si MFT devuelve **true** para el [atributo \_ \_ 3DVIDEO de compatibilidad con MFT](mft-support-3dvideo.md) .

Para obtener o establecer este atributo, llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos global de MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




