---
title: RB_DRAGMOVE mensaje (Commctrl.h)
description: Actualiza la posición de arrastre en el control rebar después de un mensaje \_ BEGINDRAG de RB anterior.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a511bd1ad13442489f3f6dbf3de1b897b30e54f9d503b30b9031426b0aedcef3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409728"
---
# <a name="rb_dragmove-message"></a>Mensaje \_ DRAGMOVE de RB

Actualiza la posición de arrastre en el control rebar después de un mensaje [**\_ BEGINDRAG de RB**](rb-begindrag.md) anterior.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valor DWORD** que contiene las nuevas coordenadas del mouse. La coordenada horizontal se encuentra en [**loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y la coordenada vertical se encuentra en [**hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Si pasa (DWORD)-1, el control rebar usará la posición del mouse la última vez que el subproceso del control se llame [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**RB \_ ENDDRAG**](rb-enddrag.md)
</dt> </dl>

 

