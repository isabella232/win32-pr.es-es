---
description: 'MFPKEY_COLORCONV_MODE propiedad : especifica si el flujo de entrada está entrelazado.'
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f86ed10873c1587aefba342392afa7f84f8c635788339d64deca18b76629255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242894"
---
# <a name="mfpkey_colorconv_mode-property"></a>Propiedad MFPKEY \_ COLORCONV \_ MODE

Especifica si el flujo de entrada está entrelazado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

Calculado por el DSP del vídeo de origen.

## <a name="applies-to"></a>Se aplica a

-   [DSP del convertidor de colores](colorconverter.md)

## <a name="remarks"></a>Comentarios

Use uno de los siguientes valores.



| Valor | Descripción |
|-------|-------------|
| 0     | progresivo |
| 2     | Interlaced  |



 

Si no se establece esta propiedad, el DSP usa el tipo de medio de entrada para determinar si el vídeo está entrelazado. Puede establecer esta propiedad para invalidar la configuración del tipo de medio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
