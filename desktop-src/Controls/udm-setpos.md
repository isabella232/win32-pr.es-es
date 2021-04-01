---
title: Mensaje de UDM_SETPOS (commctrl. h)
description: Establece la posición actual de un control de flechas con una precisión de 16 bits.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- UDM_SETPOS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150646"
---
# <a name="udm_setpos-message"></a>\_Mensaje SETPOS UDM

Establece la posición actual de un control de flechas con una precisión de 16 bits.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nueva posición del control de flechas. Si el parámetro está fuera del intervalo especificado del control, *lParam* se establecerá en el valor válido más próximo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la posición anterior.

## <a name="remarks"></a>Observaciones

Este mensaje solo admite posiciones de 16 bits. Si se han habilitado valores de 32 bits para un control de flechas con [**UDM \_ SETRANGE32**](udm-setrange32.md), use [**UDM \_ SETPOS32**](udm-setpos32.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**UDM \_ GETRANGE**](udm-getrange.md)
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> </dl>

 

 





