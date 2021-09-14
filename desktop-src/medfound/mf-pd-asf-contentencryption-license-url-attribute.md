---
description: Especifica la dirección URL de adquisición de licencias para un archivo cifrado de formato de sistemas avanzados (ASF). Este atributo corresponde al campo Dirección URL de licencia del encabezado de cifrado de contenido, definido en la especificación de ASF.
ms.assetid: fe431c38-8227-4385-ac6f-72b9982cde62
title: MF_PD_ASF_CONTENTENCRYPTION_LICENSE_URL atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5245ebbc5bfeac8b363898b4913c82b94990fc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257828"
---
# <a name="mf_pd_asf_contentencryption_license_url-attribute"></a>Atributo MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ LICENSE \_ URL

Especifica la dirección URL de adquisición de licencias para un archivo cifrado de formato de sistemas avanzados (ASF). Este atributo corresponde al campo Dirección URL de licencia del encabezado de cifrado de contenido, definido en la especificación de ASF.

## <a name="data-type"></a>Tipo de datos

Cadena de caracteres anchos

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido de ASF.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera el campo Url de licencia, lo convierte en una cadena de caracteres anchos y, a continuación, rellena una matriz terminada en NULL de **WCHAR** s. El tamaño de la matriz es igual al campo Longitud de la dirección URL de licencia del encabezado de cifrado de contenido.

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

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> </dl>

 

 




