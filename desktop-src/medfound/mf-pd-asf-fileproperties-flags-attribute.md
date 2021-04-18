---
description: Especifica si se va a difundir o buscar un archivo de formato de sistema avanzado (ASF). Este valor corresponde al campo Flags del objeto de propiedades de archivo, definido en la especificación ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: MF_PD_ASF_FILEPROPERTIES_FLAGS atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659922"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a>MF \_ PD \_ ASF \_ FILEPROPERTIES \_ atributo Flags

Especifica si se va a difundir o buscar un archivo de formato de sistema avanzado (ASF). Este valor corresponde al campo Flags del objeto de propiedades de archivo, definido en la especificación ASF.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido ASF. El valor del atributo es una operación OR bit a bit de las marcas siguientes:



| Marca | Descripción                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x01 | Marca de difusión. El archivo está en proceso de creación.                                                                                                                                                                                                                                      |
| 0x02 | Marca de búsqueda. Se busca en el archivo.<br/> Se hace búsquedas en un archivo si hay una secuencia de audio y el tamaño máximo del paquete de datos es igual al tamaño mínimo de los paquetes de datos. También se puede buscar en si el archivo tiene una secuencia de audio y una secuencia de vídeo con un objeto de índice simple coincidente.<br/> |



 

El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos ASF.

Si se establece la marca de difusión, los siguientes atributos del descriptor de presentación no son válidos:

-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ ID. de archivo**](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [**MF \_ PD \_ ASF \_ \_ hora de creación FILEPROPERTIES \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [**\_ \_ \_ paquetes FILEPROPERTIES MF de \_ ASF**](mf-pd-asf-fileproperties-packets-attribute.md)
-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ duración de la reproducción**](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ duración del envío \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)

Además, el atributo de tamaño de [**paquete de MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ \_ Max**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) y los valores de atributo de [**tamaño de \_ paquete de MF PD \_ ASF \_ FILEPROPERTIES \_ \_ \_**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) se establecen en el tamaño de paquete real.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> </dl>

 

 




