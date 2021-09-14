---
title: RB_BEGINDRAG mensaje (Commctrl.h)
description: Coloca el control rebar en modo de arrastrar y colocar. Este mensaje no hace que se envíe una notificación \_ BEGINDRAG de RBN.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- RB_BEGINDRAG controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167410"
---
# <a name="rb_begindrag-message"></a>Mensaje \_ BEGINDRAG de RB

Coloca el control rebar en modo de arrastrar y colocar. Este mensaje no hace que se envíe una notificación [ \_ BEGINDRAG de RBN.](rbn-begindrag.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda a la que afectará la operación de arrastrar y colocar.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valor DWORD** que contiene las coordenadas iniciales del mouse. La coordenada horizontal está contenida en el LOWORD y la coordenada vertical se encuentra en HIWORD. Si pasa (**DWORD**)-1, el control rebar usará la posición del mouse la última vez que el subproceso del control llamara [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Los **mensajes \_ RB BEGINDRAG,** [**RB \_ DRAGMOVE**](rb-dragmove.md)y [**RB \_ ENDDRAG**](rb-enddrag.md) permiten implementar una [**interfaz IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para un control rebar. Envíe el mensaje **\_ BEGINDRAG** de RB en respuesta a [**IDropTarget::D ragEnter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), envíe el mensaje **\_ DRAGMOVE** de RB en respuesta [**a IDropTarget::D ragOver**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)y el mensaje **RB \_ ENDDRAG** en respuesta a [**IDropTarget::D rop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) e [**IDropTarget::D ragLeave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

