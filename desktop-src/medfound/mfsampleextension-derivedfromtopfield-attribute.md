---
description: Especifica si un fotograma de vídeo desinteresado se ha derivado del campo superior o del campo inferior.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: MFSampleExtension_DerivedFromTopField atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 376cc499dd76702abb4c7054014a7c720118f33a732856202c4e654992c30985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241195"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>Atributo MFSampleExtension \_ DerivedFromTopField

Especifica si un fotograma de vídeo desinteresado se ha derivado del campo superior o del campo inferior. Este atributo se aplica a los ejemplos multimedia.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentarios

Este atributo solo es válido para muestras desenlazadas. Establezca este atributo si el marco se desenlazara mediante la interpolación de uno de los campos.

Si el valor es **TRUE,** el campo inferior se interpola desde el campo superior. Si el valor es **FALSE,** el campo superior se interpola desde el campo inferior.

Si no se establece el atributo, el marco no se ha desinterlazado. El marco es un verdadero marco progresiva o es un marco entrelazado.

Este atributo es informativo. Un desinterlacer de software podría establecer este atributo. Si se establece este atributo, proporciona una sugerencia de que puede recuperar el campo original quitando las líneas de examen interpoladas. Por ejemplo, si el atributo es **TRUE,** puede recuperar el campo superior original quitando el campo inferior interpolado.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Entrelazado de vídeo](video-interlacing.md)
</dt> </dl>

 

 




