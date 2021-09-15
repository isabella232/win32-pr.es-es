---
description: Especifica la velocidad de bits media, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de control medio.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: MFPKEY_DYN_VBR_RAVG propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468650"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>Propiedad MFPKEY \_ DYN \_ VBR \_ VBR VBG

Especifica la velocidad de bits media, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de control medio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ I4**

## <a name="remarks"></a>Observaciones

Si las [**propiedades \_ MFPKEY AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) y [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) se establecen en **VARIANT \_ TRUE,** el codificador usa la codificación VBR de control medio. En ese caso, el codificador se configura según el valor de esta propiedad y la propiedad [**\_ MFPKEY DYN \_ VBR \_ BAVG.**](mfpkey-dyn-vbr-bavgproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
