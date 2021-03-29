---
title: Mensaje de RB_BEGINDRAG (commctrl. h)
description: Coloca el control rebar en el modo de arrastrar y colocar. Este mensaje no hace que \_ se envíe una notificación de BEGINDRAG de RBN.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- RB_BEGINDRAG controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491782"
---
# <a name="rb_begindrag-message"></a>Mensaje de BEGINDRAG de RB \_

Coloca el control rebar en el modo de arrastrar y colocar. Este mensaje no hace que se envíe una notificación de [ \_ BEGINDRAG de RBN](rbn-begindrag.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda a la que afectará la operación de arrastrar y colocar.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contiene las coordenadas de inicio del mouse. La coordenada horizontal está contenida en el LOWORD y la coordenada vertical está contenida en el HIWORD. Si pasa (**DWORD**)-1, el control rebar usará la posición del mouse la última vez que el subproceso del control llamó a [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Los **mensajes \_ RB BEGINDRAG**, [**RB \_ DRAGMOVE**](rb-dragmove.md)y [**RB \_ ENDDRAG**](rb-enddrag.md) permiten implementar una interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para un control rebar. Envía el mensaje **RB \_ BEGINDRAG** en respuesta a [**IDropTarget::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), envía el mensaje **RB \_ DRAGMOVE** en respuesta a [**IDropTarget::D Ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)y el mensaje **RB \_ ENDDRAG** en respuesta a [**IDropTarget::D ROP**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) e [**IDropTarget::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

