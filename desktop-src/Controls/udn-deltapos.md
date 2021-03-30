---
title: Código de notificación de UDN_DELTAPOS (commctrl. h)
description: Lo envía el sistema operativo a la ventana primaria de un control de flechas cuando la posición del control está a punto de cambiar.
ms.assetid: 66262566-d35a-4b2a-8157-d1e789a21016
keywords:
- UDN_DELTAPOS controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802413"
---
# <a name="udn_deltapos-notification-code"></a>Código de notificación de DELTAPOS de UDN \_

Lo envía el sistema operativo a la ventana primaria de un control de flechas cuando la posición del control está a punto de cambiar. Esto sucede cuando el usuario solicita un cambio en el valor presionando la flecha arriba o abajo del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
UDN_DELTAPOS 

    lpnmud = (LPNMUPDOWN) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) que contiene información sobre el cambio de posición. El miembro **IPOS** de esta estructura contiene la posición actual del control. El miembro **iDelta** de la estructura es un entero con signo que contiene el cambio propuesto en la posición. Si el usuario hizo clic en el botón subir, se trata de un valor positivo. Si el usuario hizo clic en el botón abajo, se trata de un valor negativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para evitar el cambio en la posición del control o cero para permitir el cambio.

## <a name="remarks"></a>Observaciones

El \_ código de notificación DELTAPOS de UDN se envía antes del mensaje [**WM \_ VSCROLL**](wm-vscroll.md) o [**WM \_ HSCROLL**](wm-hscroll.md) , que realmente cambia la posición del control. Esto le permite examinar, permitir, modificar o denegar el cambio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

