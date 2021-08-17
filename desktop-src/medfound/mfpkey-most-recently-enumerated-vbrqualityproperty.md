---
description: Especifica el nivel de calidad de VBR del tipo de salida enumerado más recientemente.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68e609f8dc7b95eb9cfd4bf537af47d1a11cb4ba625f0bbc65897b008ff03a31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689799"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>MFPKEY \_ MOST \_ RECENT \_ ENUMERATED \_ VBRQUALITY Property

Especifica el nivel de calidad de VBR del tipo de salida enumerado más recientemente. Solo lectura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="remarks"></a>Comentarios

Cuando el codificador actúa como una transformación de Media Foundation (MFT) y enumera un tipo de salida en una llamada a [**IMFTransform::GetOutputAvailableType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)puede consultar el MFT para la propiedad **MFPKEY \_ MOST RECENTLY \_ \_ ENUMERATED \_ VBRQUALITY.** El valor devuelto indica la calidad de VBR del tipo de medio de salida devuelto más recientemente. A continuación, puede usar ese valor para establecer la propiedad [**\_ MFPKEY DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) del codificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista o Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
