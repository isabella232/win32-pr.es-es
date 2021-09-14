---
description: Especifica una representación numérica del equilibrio entre la subilidad del movimiento y la calidad de la imagen de la salida del códec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257647"
---
# <a name="mfpkey_crisp-property"></a>Propiedad MFPKEY \_ DE CRISP

Especifica una representación numérica del equilibrio entre la subilidad del movimiento y la calidad de la imagen de la salida del códec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCrisp

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

75

## <a name="remarks"></a>Observaciones

Este valor entero puede oscilar entre 0 y 100. Cuanto mayor sea el valor, más optimizará el códec la codificación para la calidad de la imagen de fotogramas individuales, lo que normalmente reduce la subilidad del movimiento.

Esta propiedad solo debe establecerse para la codificación de velocidad de bits constante (CBR). Las optimizaciones para la codificación de velocidad de bits variable (VBR) funcionan de forma diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




