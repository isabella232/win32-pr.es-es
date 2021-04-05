---
title: Código de notificación de MCN_SELECT (commctrl. h)
description: Se envía por un control de calendario mensual cuando el usuario realiza una selección de fecha explícita dentro de un control de calendario mensual. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079003"
---
# <a name="mcn_select-notification-code"></a>MCN \_ seleccionar código de notificación

Se envía por un control de calendario mensual cuando el usuario realiza una selección de fecha explícita dentro de un control de calendario mensual. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contiene información sobre el intervalo de fechas seleccionado actualmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El código de notificación **\_ Select MCN** es similar a [**MCN \_ SELCHANGE**](mcn-selchange.md), pero **MCN \_ Select** solo se envía como respuesta a las selecciones de fecha explícitas de un usuario. **MCN \_ SELCHANGE** se aplica a cualquier cambio de selección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





