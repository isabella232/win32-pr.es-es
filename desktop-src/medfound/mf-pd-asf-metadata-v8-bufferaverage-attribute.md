---
description: Especifica el tamaño medio de búfer necesario para un archivo de formato de sistemas avanzados (ASF) de velocidad de bits variable (VBR).
ms.assetid: 508d8670-5f5f-422b-9fa1-150115e2dbb8
title: MF_PD_ASF_METADATA_V8_BUFFERAVERAGE atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac9328d0b176df23b103c49890ffa7646ae8c02e7205df95fecc5a64e5eebc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955415"
---
# <a name="mf_pd_asf_metadata_v8_bufferaverage-attribute"></a>Atributo \_ \_ \_ \_ \_ BUFFERAVERAGE de MF PD ASF METADATA V8

Especifica el tamaño medio de búfer necesario para un archivo de formato de sistemas avanzados (ASF) de velocidad de bits variable (VBR).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los descriptores de presentación para el contenido de ASF.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo que se aplica al descriptor de presentación para el contenido de ASF.

> [!Note]  
> Este atributo solo se aplica a los archivos creados por la versión 8 del SDK Windows Media Format. Corresponde al atributo **BufferAverage** en el SDK Windows Media Format.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> </dl>

 

 




