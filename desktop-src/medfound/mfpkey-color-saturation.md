---
description: Ajusta la saturación.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: MFPKEY_COLOR_SATURATION propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579837"
---
# <a name="mfpkey_color_saturation-property"></a>Propiedad MFPKEY \_ COLOR \_ SATURATION

Ajusta la saturación.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="applies-to"></a>Se aplica a

-   [DSP de transformación de control de color](colorcontroltransform.md)

## <a name="remarks"></a>Observaciones

El ajuste de saturación se realiza multiplicando los valores Cb y Cr por una constante.

Esta propiedad tiene un intervalo de -127 a 127. Cero indica que no hay ningún cambio en la saturación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
