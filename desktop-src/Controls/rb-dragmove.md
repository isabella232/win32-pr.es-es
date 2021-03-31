---
title: Mensaje de RB_DRAGMOVE (commctrl. h)
description: Actualiza la posición de arrastre en el control rebar después de un \_ mensaje RB BEGINDRAG anterior.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- RB_DRAGMOVE controles de mensajes de Windows
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
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996727"
---
# <a name="rb_dragmove-message"></a>Mensaje de DRAGMOVE de RB \_

Actualiza la posición de arrastre en el control rebar después de un mensaje [**RB \_ BEGINDRAG**](rb-begindrag.md) anterior.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contiene las nuevas coordenadas del mouse. La coordenada horizontal está contenida en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) y la coordenada vertical está contenida en el [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Si pasa (DWORD)-1, el control rebar usará la posición del mouse la última vez que el subproceso del control llamó a [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

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

[**\_ENDDRAG RB**](rb-enddrag.md)
</dt> </dl>

 

