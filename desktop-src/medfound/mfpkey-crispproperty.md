---
description: Especifica una representación numérica del equilibrio entre la suavización del movimiento y la calidad de la imagen de la salida del códec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 177ae5e9d1c8a9aba359000e04483c8e45c44f823c9db924155dd5ef3d5989a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954265"
---
# <a name="mfpkey_crisp-property"></a>Propiedad \_ MFPKEY DE CRISP

Especifica una representación numérica del equilibrio entre la suavización del movimiento y la calidad de la imagen de la salida del códec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCrisp

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

75

## <a name="remarks"></a>Comentarios

Este valor entero puede oscilar entre 0 y 100. Cuanto mayor sea el valor, más optimizará el códec la codificación para la calidad de imagen de los fotogramas individuales, lo que normalmente reduce la suavizado del movimiento.

Esta propiedad debe establecerse solo para la codificación de velocidad de bits constante (CBR). Las optimizaciones para la codificación de velocidad de bits variable (VBR) funcionan de forma diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




