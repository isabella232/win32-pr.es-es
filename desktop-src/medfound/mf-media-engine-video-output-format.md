---
description: Establece el formato de destino de representación para el motor de medios.
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474172"
---
# <a name="mf_media_engine_video_output_format-attribute"></a>Atributo MF \_ MEDIA ENGINE VIDEO OUTPUT \_ \_ \_ \_ FORMAT

Establece el formato de destino de representación para el motor de medios.

## <a name="data-type"></a>Tipo de datos

**DXGI \_ FORMAT** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Establezca este atributo si crea el motor multimedia en modo de servidor de marco. Para obtener más información, [**vea IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). El valor del atributo es un [valor \_ DXGI FORMAT.](../direct3d9/d3dformat.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
