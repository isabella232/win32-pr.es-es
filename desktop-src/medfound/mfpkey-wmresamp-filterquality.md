---
description: Especifica la calidad de la salida.
ms.assetid: 7b45633b-7f1c-4951-a462-ad6240b9ca31
title: MFPKEY_WMRESAMP_FILTERQUALITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf00b757bd07add37f6a5b82459f37df40f9fb36ea6ef813e011adcadde196e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603375"
---
# <a name="mfpkey_wmresamp_filterquality-property"></a>Propiedad MFPKEY \_ WMRESAMP \_ FILTERQUALITY

Especifica la calidad de la salida.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="applies-to"></a>Se aplica a

-   [Audio Resampler DSP](audioresampler.md)

## <a name="remarks"></a>Comentarios

El intervalo válido de esta propiedad es de 1 a 60, ambos inclusive. Los valores más altos generan resultados de mayor calidad, pero introducen más latencia. Un valor de 1 es esencialmente el mismo que la interpolación lineal.

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

 

 
