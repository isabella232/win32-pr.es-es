---
description: Especifica una representación numérica del equilibrio entre la suavidad de movimiento y la calidad de la imagen de la salida del códec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: Propiedad MFPKEY_CRISP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812764"
---
# <a name="mfpkey_crisp-property"></a>MFPKEY \_ propiedad nítida

Especifica una representación numérica del equilibrio entre la suavidad de movimiento y la calidad de la imagen de la salida del códec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCrisp

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

75

## <a name="remarks"></a>Observaciones

Este valor entero puede oscilar entre 0 y 100. Cuanto mayor sea el valor, más el códec optimizará la codificación para la calidad de la imagen de los fotogramas individuales, lo que normalmente reduce la suavidad del movimiento.

Esta propiedad solo debe establecerse para la codificación de velocidad de bits constante (CBR). Las optimizaciones de la codificación de velocidad de bits variable (VBR) funcionan de manera diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




