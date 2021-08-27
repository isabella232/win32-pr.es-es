---
description: Contiene información sobre los códecs y formatos que se usaron para codificar el contenido en un archivo de formato de sistemas avanzados (ASF). Este atributo corresponde al objeto Codec List en el encabezado ASF, definido en la especificación asf.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: MF_PD_ASF_CODECLIST atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c512dee499dbd2d006fb695c89d59add449e64fb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471311"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>Atributo MF \_ PD \_ ASF \_ CODECLIST

Contiene información sobre los códecs y formatos que se usaron para codificar el contenido en un archivo de formato de sistemas avanzados (ASF). Este atributo corresponde al objeto Codec List en el encabezado ASF, definido en la especificación asf.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los descriptores de presentación para el contenido de ASF.

El [**método CODECASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo a partir del objeto Codec List en el encabezado ASF. Una aplicación que usa el origen [de medios de ASF](asf-media-source.md) puede obtener este atributo llamando a [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) y, a continuación, obteniendo el atributo del descriptor de presentación.

En la tabla siguiente se muestra el diseño del blob de atributos.



| Campo Objeto de lista de códecs | Tipo de datos    | Size    | Descripción                           |
|-------------------------|--------------|---------|---------------------------------------|
| Recuento de entradas de códec     | **DWORD**    | 4 bytes | Número de códecs                      |
| Entradas de códec           | **BYTE**\[\] | Varía  | Matriz de estructuras de información de códec |



 

El campo Entradas de código es una matriz de estructuras. En la tabla siguiente se muestra el formato de cada entrada:




| Campo Objeto de lista de códecs | Tipo de datos | Size | Descripción | 
|-------------------------|-----------|------|-------------|
| Tipo | <strong>DWORD</strong> | 4 bytes | Tipo de códec. Puede ser uno de los siguientes valores:<br /><ul><li>0x0001: códec de audio</li><li>0x0002: códec de vídeo</li><li>0xFFFF: Desconocido</li></ul> | 
| Longitud del nombre del códec | <strong>DWORD</strong> | 4 bytes | Tamaño de la cadena Nombre de códec, en bytes, incluido el <strong>carácter</strong> NULL. | 
| Nombre del códec | <strong>WCHAR</strong>[] | Varía | Cadena Unicode terminada en NULL que contiene el nombre del códec, como "Windows Media Video 9". | 
| Longitud de descripción del códec | <strong>DWORD</strong> | 4 bytes | Tamaño de la cadena Codec Description, en bytes, incluido el <strong>carácter</strong> NULL. | 
| Descripción del códec | <strong>WCHAR</strong>[] | Varía | Cadena Unicode terminada en NULL que contiene una descripción del códec. | 
| Longitud de la información del códec | <strong>DWORD</strong> | 4 bytes | Tamaño del campo Información de códec, en bytes. | 
| Información del códec | <strong>BYTE</strong>[] | Varía | Datos de códec. El significado de estos datos depende del códec. Normalmente, estos datos indican el formato. | 




 

> [!Note]  
> El diseño del blob de atributos no coincide exactamente con el diseño del objeto de lista de códecs en el encabezado ASF. En concreto, las longitudes de cadena se dan en bytes e incluyen el tamaño del **terminador NULL.**

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



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

 

 




