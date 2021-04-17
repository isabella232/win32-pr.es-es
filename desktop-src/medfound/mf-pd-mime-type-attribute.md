---
description: Especifica el tipo MIME del contenido.
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: MF_PD_MIME_TYPE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1893253af139a73555d3a4fd483e9f59c5ae1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659913"
---
# <a name="mf_pd_mime_type-attribute"></a>MF \_ PD \_ ( \_ atributo de tipo MIME)

Especifica el tipo MIME del contenido.

## <a name="data-type"></a>Tipo de datos

Cadena de caracteres anchos

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los descriptores de presentación.

El tipo MIME expuesto a través de [System. MIMEType](../properties/props-system-mimetype.md) para archivos multimedia puede tener una diferencia hacia elegir tipos MIME adecuados para la Alianza de redes digitales (DLNA).

El \_ \_ tipo MIME \_ de MF PD y [System. MIMEType](../properties/props-system-mimetype.md) no siempre coinciden.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



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
</dt> </dl>

 

 
