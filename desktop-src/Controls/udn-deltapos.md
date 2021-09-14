---
title: UDN_DELTAPOS de notificación (Commctrl.h)
description: Enviado por el sistema operativo a la ventana primaria de un control hacia abajo cuando la posición del control está a punto de cambiar.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS código de notificación Windows controles
topic_type:
- apiref
api_name:
- UDN_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec8f0ec2200d1f18e48c068b581b42868db197b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165457"
---
# <a name="udn_deltapos-notification-code"></a>Código de notificación DELTAPOS de UDN \_

Enviado por el sistema operativo a la ventana primaria de un control hacia abajo cuando la posición del control está a punto de cambiar. Esto sucede cuando el usuario solicita un cambio en el valor presionando la flecha arriba o abajo del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) que contiene información sobre el cambio de posición. El **miembro iPos** de esta estructura contiene la posición actual del control. El **miembro iDelta** de la estructura es un entero con signo que contiene el cambio de posición propuesto. Si el usuario ha hecho clic en el botón Arriba, este es un valor positivo. Si el usuario ha hecho clic en el botón abajo, se trata de un valor negativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para evitar el cambio en la posición del control o cero para permitir el cambio.

## <a name="remarks"></a>Observaciones

El código de notificación UDN DELTAPOS se envía antes del mensaje \_ [**WM \_ VSCROLL**](wm-vscroll.md) o [**WM \_ HSCROLL,**](wm-hscroll.md) que cambia realmente la posición del control. Esto le permite examinar, permitir, modificar o no permitir el cambio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

