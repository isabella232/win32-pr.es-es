---
description: Especifica el identificador de clave para un archivo cifrado de formato de sistemas avanzados (ASF). Este atributo corresponde al campo Id. de clave del encabezado de cifrado de contenido, definido en la especificación de ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: MF_PD_ASF_CONTENTENCRYPTION_KEYID atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edae0f324e7ab4889b21ae69714da16bfa88803db1d3aef808e4ba715522f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876438"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a>Atributo \_ \_ \_ CONTENTENCRYPTION KEYID de ASF de MF PD \_

Especifica el identificador de clave para un archivo cifrado de formato de sistemas avanzados (ASF). Este atributo corresponde al campo Id. de clave del encabezado de cifrado de contenido, definido en la especificación de ASF.

## <a name="data-type"></a>Tipo de datos

Cadena de caracteres anchos

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los descriptores de presentación para el contenido de ASF.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera el campo Id. de clave, lo convierte en una cadena de caracteres anchos y, a continuación, rellena una matriz terminada en NULL de **WCHAR** s. El tamaño de la matriz es igual al campo Longitud del identificador de clave del encabezado de cifrado de contenido.

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

 

 




