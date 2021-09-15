---
description: Especifica la velocidad de bits media, en bits por segundo, de una secuencia en un archivo de formato de sistemas avanzados (ASF). Este atributo corresponde al objeto de propiedades de velocidad de bits de flujo definido en la especificación de ASF.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: MF_SD_ASF_STREAMBITRATES_BITRATE atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580340"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a>Atributo MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATE

Especifica la velocidad de bits media, en bits por segundo, de una secuencia en un archivo de formato de sistemas avanzados (ASF). Este atributo corresponde al objeto de propiedades de velocidad de bits de flujo definido en la especificación de ASF.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo y lo establece en el descriptor de flujo. La aplicación puede crear el descriptor de secuencia para la secuencia a partir del descriptor de presentación llamando a [**ASEPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

El valor del atributo es igual al campo Average Bit Rate (Velocidad de bits media) del objeto Stream Bit Rate Properties (Propiedades de velocidad de bits de flujo).

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos de descriptor de flujo](stream-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> </dl>

 

 




