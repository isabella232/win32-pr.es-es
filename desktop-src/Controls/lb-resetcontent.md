---
title: LB_RESETCONTENT mensaje (Winuser.h)
description: Quita todos los elementos de un cuadro de lista.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- LB_RESETCONTENT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c896263cd4a695583bda299b0feeff552a05ef2c938b9df348da685821c46652
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085375"
---
# <a name="lb_resetcontent-message"></a>Mensaje \_ RESETCONTENT de LB

Quita todos los elementos de un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Si el cuadro de lista tiene un estilo dibujado por el propietario, pero no el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LBS, el propietario del cuadro de lista recibe un mensaje [**\_ DELETEITEM**](wm-deleteitem.md) de WM para cada elemento del cuadro de lista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DELETEITEM de WM \_**](wm-deleteitem.md)
</dt> </dl>

 

 





