---
title: SBM_GETRANGE mensaje (Winuser.h)
description: El mensaje GETRANGE de SBM se envía para recuperar los valores de posición mínimo y máximo \_ para el control de barra de desplazamiento.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- SBM_GETRANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167085"
---
# <a name="sbm_getrange-message"></a>Mensaje \_ GETRANGE de SBM

El **mensaje \_ GETRANGE de SBM** se envía para recuperar los valores de posición mínimo y máximo para el control de barra de desplazamiento.

Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben usar la [**función GetScrollRange.**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que **la función GetScrollRange** funcione correctamente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una variable que recibe la posición de desplazamiento mínima.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una variable que recibe la posición de desplazamiento máxima.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SETPOS de SBM \_**](sbm-setpos.md)
</dt> <dt>

[**SETRANGE de SBM \_**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

