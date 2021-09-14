---
description: Especifica el intervalo utilizado en las búsquedas de movimiento.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: MFPKEY_MOTIONSEARCHRANGE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268895"
---
# <a name="mfpkey_motionsearchrange-property"></a>Propiedad MFPKEY \_ MOTIONSEARCHRANGE

Especifica el intervalo utilizado en las búsquedas de movimiento.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCMotionSearchRange

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad puede establecerse en uno de los valores siguientes. H denota el intervalo horizontal y V denota el intervalo vertical. Todos los intervalos se dan en píxeles.



| Value | Intervalo                                |
|-------|--------------------------------------|
| 0     | +63.75/-64.0 H, +31.75/-32.0 V       |
| 1     | +127,75/-128,0 H, +63,75/-64,0 V     |
| 2     | +511.75/-512.0 H, +127.75/-128.0 V   |
| 3     | +1023.75/-1024.0 H, +255.75/-256.0 V |
| -1    | Macroblock-adaptive (automático)      |



 

Esta propiedad controla el tamaño del área de marco en la que el códec buscará un elemento que pueda haber expuesto movimiento entre fotogramas. Una ventana de búsqueda más grande le ayudará a encontrar un movimiento más rápido, pero requerirá más tiempo de CPU. Los requisitos de CPU se duplican aproximadamente en cada nivel.

El modo automático (-1) seleccionará dinámicamente el modo más eficaz.

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

 

 




