---
description: Contiene datos secretos para un archivo cifrado de formato de sistemas avanzados (ASF). Este atributo corresponde al campo Datos secretos del encabezado de cifrado de contenido, definido en la especificación de ASF.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e628bf52aa08074473f14a84ee1d1fe39fe91c130aa9848be687601b864393a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104371"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a>Atributo \_ \_ \_ CONTENTENCRYPTION \_ SECRET \_ DATA de MF PD ASF

Contiene datos secretos para un archivo cifrado de formato de sistemas avanzados (ASF). Este atributo corresponde al campo Datos secretos del encabezado de cifrado de contenido, definido en la especificación de ASF.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los descriptores de presentación para el contenido de ASF.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) rellena una matriz de bytes con el campo Datos secretos. El tamaño de la matriz es igual al campo Longitud de datos secretos del encabezado de cifrado de contenido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> </dl>

 

 




