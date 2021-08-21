---
description: Especifica la ventana de búfer, en milisegundos, para un codificador que está configurado para usar la codificación VBR de control medio.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: MFPKEY_DYN_VBR_BAVG (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77ba4d3f3d7a5587a7c8aa90771f58accd8a80864dd5a875c6c580eb9e29e01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738165"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a>Propiedad \_ MFPKEY DYN \_ VBR \_ BAVG

Especifica la ventana de búfer, en milisegundos, para un codificador que está configurado para usar la codificación VBR de control medio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ I4**

## <a name="remarks"></a>Observaciones

Si las [**propiedades \_ MFPKEY AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) y [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) se establecen en **VARIANT \_ TRUE,** el codificador usa la codificación VBR de control medio. En ese caso, el codificador se configura a sí mismo según el valor de esta propiedad y la propiedad [**\_ MFPKEY DYN \_ VBR \_ VBR VBG.**](mfpkey-dyn-vbr-ravgproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
