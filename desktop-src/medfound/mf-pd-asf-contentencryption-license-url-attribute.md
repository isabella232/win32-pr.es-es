---
description: Especifica la dirección URL de adquisición de licencias para un archivo de formato de sistema avanzado (ASF) cifrado. Este atributo corresponde al campo dirección URL de la licencia del encabezado de cifrado de contenido, definido en la especificación ASF.
ms.assetid: fe431c38-8227-4385-ac6f-72b9982cde62
title: MF_PD_ASF_CONTENTENCRYPTION_LICENSE_URL atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5245ebbc5bfeac8b363898b4913c82b94990fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497368"
---
# <a name="mf_pd_asf_contentencryption_license_url-attribute"></a>MF \_ PD \_ ASF \_ \_ atributo URL de licencia de CONTENTENCRYPTION \_

Especifica la dirección URL de adquisición de licencias para un archivo de formato de sistema avanzado (ASF) cifrado. Este atributo corresponde al campo dirección URL de la licencia del encabezado de cifrado de contenido, definido en la especificación ASF.

## <a name="data-type"></a>Tipo de datos

Cadena de caracteres anchos

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación para el contenido ASF.

El método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) recupera el campo de dirección URL de la licencia, lo convierte en una cadena de caracteres anchos y, a continuación, rellena una matriz terminada en NULL de **WCHAR** s. El tamaño de la matriz es igual al campo longitud de la dirección URL de la licencia del encabezado de cifrado de contenido.

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

 

 




