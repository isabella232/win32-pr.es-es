---
title: UDM_SETPOS mensaje (Commctrl.h)
description: Establece la posición actual de un control de arriba a abajo con precisión de 16 bits.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- UDM_SETPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f87d079a7bbe454084785cba8ed3361193224edd3e781441f4fe614533b8dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088435"
---
# <a name="udm_setpos-message"></a>Mensaje \_ SETPOS de UDM

Establece la posición actual de un control de arriba a abajo con precisión de 16 bits.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nueva posición para el control de arriba a abajo. Si el parámetro está fuera del intervalo especificado del control, *lParam* se establecerá en el valor válido más cercano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la posición anterior.

## <a name="remarks"></a>Comentarios

Este mensaje solo admite posiciones de 16 bits. Si se han habilitado valores de 32 bits para un control de flechas con [**UDM \_ SETRANGE32,**](udm-setrange32.md)use [**UDM \_ SETPOS32**](udm-setpos32.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**UDM \_ GETRANGE**](udm-getrange.md)
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> </dl>

 

 





