---
description: Especifica el nivel de calidad de VBR del tipo de salida enumerado más recientemente.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268908"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>Propiedad \_ \_ \_ VBRQUALITY ENUMERADA MÁS \_ RECIENTE de MFPKEY

Especifica el nivel de calidad de VBR del tipo de salida enumerado más recientemente. Solo lectura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="remarks"></a>Observaciones

Cuando el codificador actúa como una transformación de Media Foundation (MFT) y enumera un tipo de salida en una llamada a [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), puede consultar el MFT para la propiedad **MFPKEY \_ MOST RECENTLY \_ \_ ENUMERATED \_ VBRQUALITY.** El valor devuelto indica la calidad de VBR del tipo de medio de salida devuelto más recientemente. A continuación, puede usar ese valor para establecer la propiedad [**\_ MFPKEY DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) del codificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
