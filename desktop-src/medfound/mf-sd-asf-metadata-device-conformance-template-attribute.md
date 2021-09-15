---
description: Especifica la plantilla de conformidad de dispositivos para una secuencia en un archivo de formato de sistemas avanzados (ASF).
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574893"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a>Atributo MF \_ SD \_ ASF \_ METADATA DEVICE \_ \_ CONFORMANCE \_ TEMPLATE

Especifica la plantilla de conformidad de dispositivos para una secuencia en un archivo de formato de sistemas avanzados (ASF).

## <a name="data-type"></a>Tipo de datos

Cadena de caracteres anchos

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de flujo para el contenido de ASF. Para obtener más información sobre las plantillas de conformidad de dispositivos, vea el tema "Parámetros de plantilla de conformidad de dispositivos" en el SDK Windows Media Format.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos de ASF.

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

[**ATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**ATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos del descriptor de flujo](stream-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> </dl>

 

 




