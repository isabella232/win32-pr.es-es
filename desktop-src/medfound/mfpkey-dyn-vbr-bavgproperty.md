---
description: Especifica la ventana de búfer, en milisegundos, para un codificador que está configurado para usar la codificación VBR de media controlable.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: Propiedad MFPKEY_DYN_VBR_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648307"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a>\_Propiedad BAVG de MFPKEY DIN \_ VBR \_

Especifica la ventana de búfer, en milisegundos, para un codificador que está configurado para usar la codificación VBR de media controlable.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

**VT \_ I4**

## <a name="remarks"></a>Observaciones

Si las propiedades [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) y [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) están establecidas en **Variant \_ true**, el codificador usa la codificación VBR de media controlable. En ese caso, el codificador se configura a sí mismo según el valor de esta propiedad y la propiedad [**RAVG de MFPKEY \_ DYN \_ VBR \_**](mfpkey-dyn-vbr-ravgproperty.md) .

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

 

 
