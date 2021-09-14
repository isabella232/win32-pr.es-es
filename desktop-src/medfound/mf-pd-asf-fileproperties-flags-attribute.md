---
description: Especifica si un archivo de formato de sistemas avanzados (ASF) se difunde o se puede buscar. Este valor corresponde al campo Flags del objeto Propiedades de archivo, definido en la especificación de ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: MF_PD_ASF_FILEPROPERTIES_FLAGS atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363927"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a>Atributo \_ MF PD \_ ASF \_ FILEPROPERTIES \_ FLAGS

Especifica si un archivo de formato de sistemas avanzados (ASF) se difunde o se puede buscar. Este valor corresponde al campo Flags del objeto Propiedades de archivo, definido en la especificación de ASF.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido de ASF. El valor del atributo es un OR bit a bit de las marcas siguientes:



| Marca | Descripción                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x01 | Marca de difusión. El archivo está en proceso de creación.                                                                                                                                                                                                                                      |
| 0x02 | Marca que se puede buscar. El archivo es buscable.<br/> Se puede buscar un archivo si hay una secuencia de audio y el tamaño máximo del paquete de datos es igual al tamaño mínimo del paquete de datos. También puede ser buscable si el archivo tiene una secuencia de audio y una secuencia de vídeo con un objeto de índice simple correspondiente.<br/> |



 

El [**método IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera este atributo a partir de los metadatos de ASF.

Si se establece la marca de difusión, los atributos siguientes en el descriptor de presentación no son válidos:

-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ FILE \_ ID**](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ CREATION \_ TIME**](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [**PAQUETES \_ \_ FILEPROPERTIES DE ASF DE MF PD \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)
-   [**DURACIÓN \_ DE REPRODUCCIÓN DE FILEPROPERTIES DE MF PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [**DURACIÓN DEL ENVÍO DE ARCHIVOS ASF DE \_ MF \_ \_ \_ PDPROPIEDADES \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)

Además, los valores de atributo [**MF \_ PD \_ ASF \_ FILEPROPERTIES MAX PACKET \_ \_ \_ SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) y [**MF PD \_ \_ ASF \_ FILEPROPERTIES MIN PACKET \_ \_ \_ SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) se establecen en el tamaño real del paquete.

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> </dl>

 

 




