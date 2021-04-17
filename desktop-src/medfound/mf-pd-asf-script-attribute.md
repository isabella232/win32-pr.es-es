---
description: Especifica una lista de comandos de script y los parámetros de un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de comando de script del encabezado ASF, definido en la especificación ASF.
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: MF_PD_ASF_SCRIPT atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716421"
---
# <a name="mf_pd_asf_script-attribute"></a>MF \_ PD \_ ASF \_ atributo de script

Especifica una lista de comandos de script y los parámetros de un archivo de formato de sistema avanzado (ASF). Este atributo corresponde al objeto de comando de script del encabezado ASF, definido en la especificación ASF.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido ASF.

El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea el descriptor de presentación y genera este atributo desde el encabezado del objeto de comando de script. En la tabla siguiente se muestra el formato del BLOB:



| Campo de objeto de comando de script | Tipo de datos    | Tamaño    | Descripción               |
|-----------------------------|--------------|---------|---------------------------|
| Recuento de comandos              | **DWORD**    | 4 bytes | Número de comandos de script |
| Tipo de comando, comandos      | **BYTES**\[\] | Varía  | Matriz de comandos de script  |



 

El primer **valor DWORD** es el número de comandos de script, seguidos de una matriz de comandos. Cada comando de script tiene el siguiente formato:



| Campo de objeto de comando de script | Tipo de datos     | Tamaño    | Descripción                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| Longitud del nombre de comando         | **DWORD**     | 4 bytes | Tamaño de la cadena de comandos, en bytes, incluido el carácter nulo.      |
| Nombre de comando                | **WCHAR**\[\] | Varía  | Cadena terminada en null que contiene el comando de script.                 |
| Longitud del nombre del tipo de comando    | **DWORD**     | 4 bytes | Tamaño de la cadena de tipo de comando, en bytes, incluido el carácter nulo. |
| Nombre del tipo de comando           | **WCHAR**\[\] | Varía  | Cadena terminada en null que contiene el tipo de comando.                   |
| Tiempo de presentación           | **DWORD**     | 4 bytes | Tiempo de presentación del comando en milisegundos.                        |



 

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

 

 




