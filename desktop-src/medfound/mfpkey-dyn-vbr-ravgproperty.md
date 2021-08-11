---
description: Especifica la velocidad de bits media, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de control medio.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: MFPKEY_DYN_VBR_RAVG propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ee3d3a9b9a60b664041b9c6f84c38b8da9ceef87f73177f2ace792cf043992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242617"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>Propiedad MFPKEY \_ DYN \_ VBR \_ VBR VBG

Especifica la velocidad de bits media, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de control medio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

**VT \_ I4**

## <a name="remarks"></a>Comentarios

Si las [**propiedades \_ MFPKEY AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) y [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) se establecen en **VARIANT \_ TRUE,** el codificador usa la codificación VBR de control medio. En ese caso, el codificador se configura según el valor de esta propiedad y la propiedad [**\_ MFPKEY DYN \_ VBR \_ BAVG.**](mfpkey-dyn-vbr-bavgproperty.md)

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

 

 
