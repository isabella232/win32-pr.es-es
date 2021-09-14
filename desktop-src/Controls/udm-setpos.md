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
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165482"
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

## <a name="remarks"></a>Observaciones

Este mensaje solo admite posiciones de 16 bits. Si se han habilitado valores de 32 bits para un control de flechas con [**UDM \_ SETRANGE32,**](udm-setrange32.md)use [**UDM \_ SETPOS32**](udm-setpos32.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**UDM \_ GETRANGE**](udm-getrange.md)
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> </dl>

 

 





