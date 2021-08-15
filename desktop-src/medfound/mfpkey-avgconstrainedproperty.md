---
description: Especifica si el codificador usa la codificación VBR de control medio.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: MFPKEY_AVGCONSTRAINED (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e7231cb3807be8f4467592ac0138a75ea277bdf8a13dfb3564d3572036e7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874099"
---
# <a name="mfpkey_avgconstrained-property"></a>Propiedad AVGCONSTRAINED de MFPKEY \_

Especifica si el codificador usa la codificación VBR de control medio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentarios

Si esta propiedad y la propiedad [**\_ MFPKEY VBRENABLED**](mfpkey-vbrenabledproperty.md) están establecidas en **VARIANT \_ TRUE,** el codificador usa la codificación VBR de control medio. En ese caso, el codificador se configura según los valores de [**MFPKEY \_ DYN \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) y [**MFPKEY \_ DYN \_ VBR \_ VBR VBG**](mfpkey-dyn-vbr-ravgproperty.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
