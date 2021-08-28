---
description: Especifica los marcadores en un archivo de formato de sistemas avanzados (ASF). Este atributo corresponde al objeto Marker en el encabezado ASF, definido en la especificación asf.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: MF_PD_ASF_MARKER atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89210324b8cde1952fdee137723024f2f6911d6b295b213a4959cc113e01b8ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691937"
---
# <a name="mf_pd_asf_marker-attribute"></a>Atributo \_ MF PD \_ ASF \_ MARKER

Especifica los marcadores en un archivo de formato de sistemas avanzados (ASF). Este atributo corresponde al objeto Marker en el encabezado ASF, definido en la especificación asf.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los descriptores de presentación para el contenido de ASF.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo a partir del objeto Marker. En la tabla siguiente se muestra el formato del blob:



| Campo Objeto de marcador | Tipo de datos    | Size    | Descripción       |
|---------------------|--------------|---------|-------------------|
| Recuento de marcadores       | **DWORD**    | 4 bytes | Número de marcadores |
| Marcadores             | **Byte**\[\] | Varía  | Matriz de marcadores  |



 

El primer **DWORD** es el número de marcadores, seguido de una matriz de marcadores. Cada marcador tiene el formato siguiente:



| Campo Objeto de marcador       | Tipo de datos     | Size    | Descripción                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| Longitud de descripción del marcador | **DWORD**     | 4 bytes | Tamaño de la cadena de descripción, en bytes, incluido el carácter NULL.           |
| Descripción del marcador        | **Wchar**\[\] | Varía  | Cadena terminada en NULL que describe el marcador.                                 |
| Tiempo de presentación         | **LONGLONG**  | 8 bytes | Tiempo de presentación del marcador, en unidades de 100 nanosegundos.                         |
| Hora de envío                 | **LONGLONG**  | 8 bytes | Hora de envío de la entrada del marcador, en milisegundos.                                   |
| Offset                    | **UINT64**    | 8 bytes | Desplazamiento, en bytes, en el objeto de datos que especifica la posición del mercado. |



 

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

 

 




