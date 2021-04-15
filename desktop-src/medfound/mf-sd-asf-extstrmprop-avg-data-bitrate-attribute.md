---
description: Especifica la velocidad de bits de datos media, en bits por segundo, de una secuencia en un archivo de formato de sistema avanzado (ASF).
ms.assetid: 3a0b39ab-e9a9-49df-a321-a88559aec16f
title: MF_SD_ASF_EXTSTRMPROP_AVG_DATA_BITRATE atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18789fbd18f063c59de712cf1b1b6bdac1c38a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648515"
---
# <a name="mf_sd_asf_extstrmprop_avg_data_bitrate-attribute"></a>MF \_ SD \_ ASF \_ EXTSTRMPROP \_ promedio \_ de \_ velocidad de bits de datos

Especifica la velocidad de bits de datos media, en bits por segundo, de una secuencia en un archivo de formato de sistema avanzado (ASF).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de flujo para el contenido ASF. Se corresponde con el campo de velocidad de bits de datos del objeto Extended Stream Properties y define la tasa de fugas usada en el modelo de "depósito de fugas". Para obtener más información, consulte la especificación ASF.

El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF. La aplicación puede crear el descriptor de flujo para la secuencia desde el descriptor de presentación mediante una llamada a [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos de descriptor de secuencia](stream-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> </dl>

 

 




