---
title: SBM_GETPOS mensaje (Winuser.h)
description: El mensaje GETPOS de SBM se envía para recuperar la posición actual del \_ cuadro de desplazamiento de un control de barra de desplazamiento.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- SBM_GETPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167086"
---
# <a name="sbm_getpos-message"></a>Mensaje \_ GETPOS de SBM

El **mensaje \_ GETPOS de SBM** se envía para recuperar la posición actual del cuadro de desplazamiento de un control de barra de desplazamiento. La posición actual es un valor relativo que depende del intervalo de desplazamiento actual. Por ejemplo, si el intervalo de desplazamiento es de 0 a 100 y el cuadro de desplazamiento está en el centro de la barra, la posición actual es 50.

Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben usar la [**función GetScrollPos.**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la **función GetScrollPos** funcione correctamente.

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

El valor devuelto es la posición actual del cuadro de desplazamiento en la barra de desplazamiento.

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

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SETPOS de SBM \_**](sbm-setpos.md)
</dt> <dt>

[**SETRANGE de SBM \_**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

