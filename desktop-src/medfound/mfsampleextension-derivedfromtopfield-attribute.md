---
description: Especifica si un fotograma de vídeo desentrelazado se ha derivado del campo superior o del campo inferior.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: MFSampleExtension_DerivedFromTopField atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696886"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>\_Atributo DerivedFromTopField de MFSampleExtension

Especifica si un fotograma de vídeo desentrelazado se ha derivado del campo superior o del campo inferior. Este atributo se aplica a los ejemplos de medios.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

Este atributo solo es válido para los ejemplos desentrelazados. Establezca este atributo si el marco se desentrelaza mediante la interpolación de uno de los campos.

Si el valor es **true**, el campo inferior se interpola a partir del campo superior. Si el valor es **false**, el campo superior se interpola a partir del campo inferior.

Si no se establece el atributo, el marco no se ha desentrelazado. El marco es un fotograma progresivo verdadero o es un marco entrelazado.

Este atributo es informativo. Un desentrelazador de software podría establecer este atributo. Si se establece este atributo, se proporciona una sugerencia que permite recuperar el campo original quitando las líneas de recorrido interpoladas. Por ejemplo, si el atributo es **true**, puede recuperar el campo superior original quitando el campo interpolado inferior.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Entrelazado de vídeo](video-interlacing.md)
</dt> </dl>

 

 




