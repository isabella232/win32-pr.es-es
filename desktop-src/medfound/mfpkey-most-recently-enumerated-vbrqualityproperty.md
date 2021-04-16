---
description: Especifica el nivel de calidad VBR del tipo de salida enumerado más recientemente.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: Propiedad MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650163"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>\_ \_ \_ Propiedad VBRQUALITY enumerada más reciente de MFPKEY \_

Especifica el nivel de calidad VBR del tipo de salida enumerado más recientemente. Solo lectura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="remarks"></a>Observaciones

Cuando el codificador actúa como una transformación de Media Foundation (MFT) y enumera un tipo de salida en una llamada a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), puede consultar la MFT de la propiedad **\_ \_ \_ \_ VBRQUALITY enumerada más recientemente de MFPKEY** . El valor devuelto indica la calidad VBR del tipo de medio de salida devuelto más recientemente. Después, puede usar ese valor para establecer la [**propiedad \_ \_ VBRQUALITY deseada de MFPKEY**](mfpkey-desired-vbrqualityproperty.md) del codificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista o Windows 7<br/>                                                   |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY \_ restricción de \_ VBRQUALITY enumerada \_**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
