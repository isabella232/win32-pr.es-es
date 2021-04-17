---
description: Especifica los marcadores en un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de marcador en el encabezado ASF, definido en la especificación ASF.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: MF_PD_ASF_MARKER atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688518"
---
# <a name="mf_pd_asf_marker-attribute"></a>MF \_ PD \_ ASF \_ atributo de marcador

Especifica los marcadores en un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de marcador en el encabezado ASF, definido en la especificación ASF.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido ASF.

El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo a partir del objeto de marcador. En la tabla siguiente se muestra el formato del BLOB:



| Campo de objeto de marcador | Tipo de datos    | Tamaño    | Descripción       |
|---------------------|--------------|---------|-------------------|
| Recuento de marcadores       | **DWORD**    | 4 bytes | Número de marcadores |
| Marcadores             | **BYTES**\[\] | Varía  | Matriz de marcadores  |



 

El primer **valor DWORD** es el número de marcadores seguido de una matriz de marcadores. Cada marcador tiene el formato siguiente:



| Campo de objeto de marcador       | Tipo de datos     | Tamaño    | Descripción                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| Longitud de la descripción del marcador | **DWORD**     | 4 bytes | Tamaño de la cadena de descripción, en bytes, incluido el carácter nulo.           |
| Descripción del marcador        | **WCHAR**\[\] | Varía  | Cadena terminada en null que describe el marcador.                                 |
| Tiempo de presentación         | **LONGLONG**  | 8 bytes | Tiempo de presentación del marcador, en unidades de 100-nanosegundos.                         |
| Hora de envío                 | **LONGLONG**  | 8 bytes | Hora de envío de la entrada de marcador, en milisegundos.                                   |
| Offset                    | **UINT64**    | 8 bytes | Desplazamiento, en bytes, en el objeto de datos que especifica la posición del mercado. |



 

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

 

 




