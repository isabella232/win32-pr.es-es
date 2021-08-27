---
title: SB_SIMPLE mensaje (Commctrl.h)
description: Especifica si una ventana de estado muestra texto simple o muestra todas las partes de la ventana establecidas por un mensaje SB \_ SETPARTS anterior.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- SB_SIMPLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f0a896c9adcab6886151753761c62aefb8f4dc6ee21b7e85bb7507bda11f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132215"
---
# <a name="sb_simple-message"></a>Sb \_ SIMPLE message (Mensaje SIMPLE de SB)

Especifica si una ventana de estado muestra texto simple o muestra todas las partes de la ventana establecidas por un mensaje [**SB \_ SETPARTS**](sb-setparts.md) anterior.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Mostrar marca de tipo. Si este parámetro es **TRUE,** la ventana muestra texto simple. Si es **FALSE,** muestra varias partes.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Comentarios

Si la ventana de estado se cambia de no simple a simple, o viceversa, la ventana se vuelve a dibujar inmediatamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





