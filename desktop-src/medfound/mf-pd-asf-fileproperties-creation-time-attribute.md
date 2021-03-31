---
description: Especifica la fecha y hora en que se creó un archivo de formato de sistema avanzado (ASF).
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: MF_PD_ASF_FILEPROPERTIES_CREATION_TIME atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f48f251f5ff9c7332de0e355c58782ed98fad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001116"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a>MF \_ PD \_ ASF \_ FILEPROPERTIES \_ atributo de hora de creación \_

Especifica la fecha y hora en que se creó un archivo de formato de sistema avanzado (ASF).

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido ASF. El valor del atributo es una estructura **FILETIME** , que se documenta en el Windows SDK.

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

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> </dl>

 

 




