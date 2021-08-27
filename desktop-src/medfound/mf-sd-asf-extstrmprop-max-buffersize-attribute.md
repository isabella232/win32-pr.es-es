---
description: Especifica el tamaño máximo de búfer, en bytes, necesario para una secuencia en un archivo de formato de sistemas avanzados (ASF).
ms.assetid: 1704a70a-a52b-4e7d-8a32-d0c4e97f8cc2
title: MF_SD_ASF_EXTSTRMPROP_MAX_BUFFERSIZE atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399f6af425020a72caf6185da18f7747c037a71245b8e8d841d886d7b7eabd18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113735"
---
# <a name="mf_sd_asf_extstrmprop_max_buffersize-attribute"></a>Atributo MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE

Especifica el tamaño máximo de búfer, en bytes, necesario para una secuencia en un archivo de formato de sistemas avanzados (ASF).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los descriptores de flujo para el contenido de ASF. Corresponde al campo Tamaño de búfer alternativo del objeto Propiedades de secuencia extendidas. Para obtener más información, consulte la especificación de ASF.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos de ASF. La aplicación puede crear el descriptor de secuencia para la secuencia a partir del descriptor de presentación llamando a [**ASEPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).

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

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Atributos de descriptor de flujo](stream-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> </dl>

 

 




