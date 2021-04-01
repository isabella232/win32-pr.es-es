---
title: Código de notificación de HDN_ITEMCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- HDN_ITEMCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905519"
---
# <a name="hdn_itemclick-notification-code"></a>Código de notificación de ITEMCLICK de HDN \_

Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que identifica el control de encabezado y especifica el índice del elemento de encabezado en el que se hizo clic y el botón del mouse que se usa para hacer clic en el elemento. El miembro **pItem** se establece en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Un control de encabezado envía este código de notificación cuando el usuario suelta el botón primario del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ ITEMCLICKW** (Unicode) y **HDN \_ ITEMCLICKA** (ANSI)<br/>               |



 

 





