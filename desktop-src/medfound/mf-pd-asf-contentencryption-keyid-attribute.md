---
description: Especifica el identificador de clave para un archivo de formato de sistema avanzado (ASF) cifrado. Este atributo corresponde al campo de identificador de clave del encabezado de cifrado de contenido, definido en la especificación ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: MF_PD_ASF_CONTENTENCRYPTION_KEYID atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154189"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a>MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ atributo de ID. de la ID.

Especifica el identificador de clave para un archivo de formato de sistema avanzado (ASF) cifrado. Este atributo corresponde al campo de identificador de clave del encabezado de cifrado de contenido, definido en la especificación ASF.

## <a name="data-type"></a>Tipo de datos

Cadena de caracteres anchos

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido ASF.

El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera el campo de ID. de clave, lo convierte en una cadena de caracteres anchos y, a continuación, rellena una matriz terminada en NULL de **WCHAR** s. El tamaño de la matriz es igual al campo de longitud de identificador de clave del encabezado de cifrado de contenido.

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

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> </dl>

 

 




