---
description: Contiene información acerca de los códecs y formatos que se usaron para codificar el contenido en un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de lista de códecs del encabezado ASF, definido en la especificación ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: MF_PD_ASF_CODECLIST atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697524"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>MF \_ PD \_ ASF \_ atributo CODECLIST

Contiene información acerca de los códecs y formatos que se usaron para codificar el contenido en un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de lista de códecs del encabezado ASF, definido en la especificación ASF.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido ASF.

El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo a partir del objeto de lista de códecs del encabezado ASF. Una aplicación que usa el [origen de medios ASF](asf-media-source.md) puede obtener este atributo llamando a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) y, a continuación, obteniendo el atributo del descriptor de presentación.

En la tabla siguiente se muestra el diseño del BLOB de atributo.



| Campo de objeto de lista de códecs | Tipo de datos    | Tamaño    | Descripción                           |
|-------------------------|--------------|---------|---------------------------------------|
| Recuento de entradas de códec     | **DWORD**    | 4 bytes | Número de códecs                      |
| Entradas de códec           | **BYTES**\[\] | Varía  | Matriz de estructuras de información de códecs |



 

El campo entradas de código es una matriz de estructuras. En la tabla siguiente se muestra el formato de cada entrada:



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo de objeto de lista de códecs</th>
<th>Tipo de datos</th>
<th>Tamaño</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tipo</td>
<td><strong>DWORD</strong></td>
<td>4 bytes</td>
<td>Tipo de códec. Puede ser uno de los siguientes valores:<br/>
<ul>
<li>0x0001: códec de audio</li>
<li>0x0002: códec de vídeo</li>
<li>0xFFFF: desconocido</li>
</ul></td>
</tr>
<tr class="even">
<td>Longitud del nombre del códec</td>
<td><strong>DWORD</strong></td>
<td>4 bytes</td>
<td>Tamaño de la cadena del nombre del códec, en bytes, incluido el carácter <strong>nulo</strong> .</td>
</tr>
<tr class="odd">
<td>Nombre del códec</td>
<td><strong>WCHAR</strong>[]</td>
<td>Varía</td>
<td>Cadena Unicode terminada en null que contiene el nombre del códec, como &quot; Windows Media Video 9 &quot; .</td>
</tr>
<tr class="even">
<td>Longitud de la descripción del códec</td>
<td><strong>DWORD</strong></td>
<td>4 bytes</td>
<td>Tamaño de la cadena de Descripción del códec, en bytes, incluido el carácter <strong>nulo</strong> .</td>
</tr>
<tr class="odd">
<td>Descripción del códec</td>
<td><strong>WCHAR</strong>[]</td>
<td>Varía</td>
<td>Una cadena Unicode terminada en null que contiene una descripción del códec.</td>
</tr>
<tr class="even">
<td>Longitud de información de códec</td>
<td><strong>DWORD</strong></td>
<td>4 bytes</td>
<td>Tamaño del campo de información del códec, en bytes.</td>
</tr>
<tr class="odd">
<td>Información del códec</td>
<td><strong>Byte</strong>[]</td>
<td>Varía</td>
<td>Datos de códec. El significado de estos datos depende del códec. Normalmente, estos datos indican el formato.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> El diseño del BLOB de atributo no coincide exactamente con el diseño del objeto de lista de códecs del encabezado ASF. En concreto, las longitudes de cadena se proporcionan en bytes e incluyen el tamaño del terminador **null** .

 

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

 

 




