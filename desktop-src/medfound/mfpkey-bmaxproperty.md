---
description: Especifica la ventana de búfer, en milisegundos, de una secuencia restringida de velocidad de bits variable (VBR) a su velocidad de bits máxima (especificada por MFPKEY \_ RMAX).
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: MFPKEY_BMAX propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87eba5d476cce43063b139d7ca94d8bb518c7965e9bccde571438e4c3e095c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873735"
---
# <a name="mfpkey_bmax-property"></a>Propiedad BMAX de MFPKEY \_

Especifica la ventana de búfer, en milisegundos, de una secuencia de velocidad de bits variable (VBR) restringida a su velocidad de bits máxima (especificada por [MFPKEY \_ RMAX).](mfpkey-rmaxproperty.md)

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBMax

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

No hay valor predeterminado.

## <a name="remarks"></a>Comentarios

Debe establecer este valor para la codificación VBR con restricciones máximas. Después de comenzar a procesar ejemplos, no debe consultar este valor hasta que haya terminado de codificar la secuencia. El códec interpreta una solicitud para este valor como una señal de que la sesión de codificación ha terminado; el ejemplo siguiente que se procesa se trata como el principio de una nueva sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




