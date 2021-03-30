---
title: Mensaje de LVM_REDRAWITEMS (commctrl. h)
description: Fuerza un control de vista de lista para volver a dibujar un intervalo de elementos. Puede enviar este mensaje explícitamente o mediante la \_ macro RedrawItems de ListView.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079353"
---
# <a name="lvm_redrawitems-message"></a>\_Mensaje REDRAWITEMS LVM

Fuerza un control de vista de lista para volver a dibujar un intervalo de elementos. Puede enviar este mensaje explícitamente o mediante la macro [**\_ RedrawItems de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del primer elemento que se va a volver a dibujar.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice del último elemento que se va a volver a dibujar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Los elementos especificados no se redibujan realmente hasta que la ventana de la vista de lista recibe un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) para volver a pintar. Para volver a dibujar inmediatamente, llame a la función [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) después de usar esta macro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

