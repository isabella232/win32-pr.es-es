---
description: Especifica una lista de comandos de script y los parámetros de un archivo de formato de sistemas avanzados (ASF). Este atributo corresponde al objeto De comando de script en el encabezado ASF, definido en la especificación de ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: MF_PD_ASF_SCRIPT atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b98a078b0196add597ab184703306a7b2eba260082e3544ae84697b70bf71822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740726"
---
# <a name="mf_pd_asf_script-attribute"></a>Atributo \_ MF PD \_ ASF \_ SCRIPT

Especifica una lista de comandos de script y los parámetros de un archivo de formato de sistemas avanzados (ASF). Este atributo corresponde al objeto De comando de script en el encabezado ASF, definido en la especificación de ASF.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido de ASF.

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo a partir del encabezado Script Command Object. En la tabla siguiente se muestra el formato del blob:



| Campo Objeto de comando de script | Tipo de datos    | Size    | Descripción               |
|-----------------------------|--------------|---------|---------------------------|
| Recuento de comandos              | **DWORD**    | 4 bytes | Número de comandos de script |
| Tipo de comando, Comandos      | **Byte**\[\] | Varía  | Matriz de comandos de script  |



 

El primer **DWORD** es el número de comandos de script, seguido de una matriz de comandos. Cada comando de script tiene el formato siguiente:



| Campo Objeto de comando de script | Tipo de datos     | Size    | Descripción                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| Longitud del nombre del comando         | **DWORD**     | 4 bytes | Tamaño de la cadena de comando, en bytes, incluido el carácter NULL.      |
| Nombre de comando                | **Wchar**\[\] | Varía  | Cadena terminada en NULL que contiene el comando de script.                 |
| Longitud del nombre del tipo de comando    | **DWORD**     | 4 bytes | Tamaño de la cadena de tipo de comando, en bytes, incluido el carácter NULL. |
| Nombre del tipo de comando           | **Wchar**\[\] | Varía  | Cadena terminada en NULL que contiene el tipo de comando.                   |
| Tiempo de presentación           | **DWORD**     | 4 bytes | Tiempo de presentación del comando en milisegundos.                        |



 

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

 

 




