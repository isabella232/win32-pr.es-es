---
description: Especifica la velocidad de fotogramas de entrada como proporción.
ms.assetid: 8988fc7e-02bd-43ea-8934-e3af44a38bc5
title: MFPKEY_CONV_INPUTFRAMERATE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5db89db9fe9f762d0298d1cb1e59fae963fa8d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257655"
---
# <a name="mfpkey_conv_inputframerate-property"></a>Propiedad INPUTFRAMERATE de MFPKEY \_ CONV \_

Especifica la velocidad de fotogramas de entrada como proporción.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ UI8

## <a name="applies-to"></a>Se aplica a

-   [Convertidor de velocidad de fotogramas](framerateconverter.md)

## <a name="remarks"></a>Observaciones

Almacene el numerador en los 4 bytes más altos y el denominador en los 4 bytes inferiores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
