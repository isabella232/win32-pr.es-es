---
description: Especifica el desplazamiento, en bytes, desde el inicio de un archivo de formato de sistemas avanzados (ASF) hasta el inicio del primer paquete de datos.
ms.assetid: 5145d952-19d9-4bf8-9046-0b5d28f5e641
title: MF_PD_ASF_DATA_START_OFFSET atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125ae1263467afe7e0aa9017e8049b13796538fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468683"
---
# <a name="mf_pd_asf_data_start_offset-attribute"></a>Atributo MF \_ PD \_ ASF \_ DATA START \_ \_ OFFSET

Especifica el desplazamiento, en bytes, desde el inicio de un archivo de formato de sistemas avanzados (ASF) hasta el inicio del primer paquete de datos.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido de ASF.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos de ASF.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> </dl>

 

 




