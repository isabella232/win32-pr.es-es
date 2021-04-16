---
description: Especifica la plantilla de conformidad de dispositivos de una secuencia en un archivo de formato de sistema avanzado (ASF).
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716150"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a>MF \_ SD \_ ASF \_ \_ atributo de \_ plantilla de cumplimiento de dispositivos de metadatos \_

Especifica la plantilla de conformidad de dispositivos de una secuencia en un archivo de formato de sistema avanzado (ASF).

## <a name="data-type"></a>Tipo de datos

Cadena de caracteres anchos

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de flujo para el contenido ASF. Para obtener más información acerca de las plantillas de conformidad de dispositivos, consulte el tema "parámetros de plantilla de conformidad de dispositivos" en el SDK de Windows Media Format.

El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos de descriptor de secuencia](stream-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> </dl>

 

 




