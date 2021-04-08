---
description: Especifica la velocidad de bits promedio, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de tamaño medio.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: Propiedad MFPKEY_DYN_VBR_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001634"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>\_Propiedad RAVG de MFPKEY DIN \_ VBR \_

Especifica la velocidad de bits promedio, en bits por segundo, para un codificador que está configurado para usar la codificación VBR de tamaño medio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ I4**

## <a name="remarks"></a>Observaciones

Si las propiedades [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) y [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) están establecidas en **Variant \_ true**, el codificador usa la codificación VBR de media controlable. En ese caso, el codificador se configura a sí mismo según el valor de esta propiedad y la propiedad [**BAVG de MFPKEY \_ DYN \_ VBR \_**](mfpkey-dyn-vbr-bavgproperty.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
