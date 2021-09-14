---
description: Especifica el aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Ac-3 de Dolby.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Propiedad AVDecDDDynamicRangeScaleLow (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b68b1d4376d9ba15859be943ded23458fe16d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162137"
---
# <a name="avdecdddynamicrangescalelow-property"></a>Propiedad AVDecDDDynamicRangeScaleLow

Especifica el aumento de bajo nivel cuando el descodificador realiza el control de intervalo dinámico en una secuencia de audio Ac-3 de Dolby.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecDDDynamicRangeScaleLow**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad tiene el intervalo siguiente.



| Value | Descripción                                                    |
|-------|----------------------------------------------------------------|
| 0     | Sin compresión de intervalo dinámico. Conserve el intervalo dinámico completo. |
| 100   | Aplique la compresión de intervalo dinámico completa.                          |



 

## <a name="remarks"></a>Observaciones

Esta propiedad solo se aplica cuando el valor de la propiedad [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) es eAVDecDDOperationalMode \_ LINE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| aplicaciones para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP de 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




