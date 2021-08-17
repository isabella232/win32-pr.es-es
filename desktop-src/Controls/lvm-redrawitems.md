---
title: LVM_REDRAWITEMS mensaje (Commctrl.h)
description: Fuerza a un control de vista de lista a volver a dibujar un intervalo de elementos. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ RedrawItems.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS controles de Windows mensaje
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
ms.openlocfilehash: 53fbee43ff8cfcbb14ab357b6e76ab709df3e4a797143d5c4fa2c9b1179153af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261735"
---
# <a name="lvm_redrawitems-message"></a>Mensaje \_ LVM REDRAWITEMS

Fuerza a un control de vista de lista a volver a dibujar un intervalo de elementos. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ RedrawItems.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems)

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

Devuelve **TRUE si** se realiza correctamente o FALSE en **caso** contrario.

## <a name="remarks"></a>Observaciones

Los elementos especificados no se dibujan realmente hasta que la ventana de vista de lista recibe un [**mensaje \_ WM PAINT**](/windows/desktop/gdi/wm-paint) para volver a dibujar. Para volver a dibujar inmediatamente, llame a [**la función UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) después de usar esta macro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

