---
description: Especifica si un archivo de formato de sistemas avanzados (ASF) usa la codificación de velocidad de bits variable (VBR).
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: MF_PD_ASF_METADATA_IS_VBR atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5863d5366fd94e230040f81d3f67f4c75fd3fe3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263292"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a>MF \_ PD \_ ASF METADATA IS \_ \_ \_ VBR attribute

Especifica si un archivo de formato de sistemas avanzados (ASF) usa la codificación de velocidad de bits variable (VBR).

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido de ASF. Si el valor es **TRUE,** el archivo se ha codificado mediante VBR. Si el valor es **FALSE o** el atributo no está presente, el archivo no usa la codificación VBR.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo y lo establece en el descriptor de presentación.

> [!Note]  
> Este atributo corresponde al atributo **IsVBR** en el SDK Windows Media Format.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 




