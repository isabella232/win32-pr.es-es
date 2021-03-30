---
title: Código de notificación de TVN_GETINFOTIP (commctrl. h)
description: Enviado por un control de vista de árbol que tiene el estilo de recuadro de TV \_ . Este código de notificación se envía cuando el control solicita información de texto adicional que se va a mostrar en una información sobre herramientas. El código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802840"
---
# <a name="tvn_getinfotip-notification-code"></a>Código de notificación de GETINFOTIP de TVN \_

Enviado por un control de vista de árbol que tiene el estilo de recuadro de [**TV \_**](tree-view-control-window-styles.md) . Este código de notificación se envía cuando el control solicita información de texto adicional que se va a mostrar en una información sobre herramientas. El código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto para este código de notificación.

## <a name="remarks"></a>Observaciones

Este código de notificación solo lo envían los controles de vista de árbol que tienen el estilo de recuadro de [**TV \_**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ GETINFOTIPW** (Unicode) y **TVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





