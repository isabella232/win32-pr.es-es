---
title: Código de notificación de TTN_NEEDTEXT (commctrl. h)
description: Lo envía un control ToolTip para recuperar la información necesaria para mostrar una ventana de información sobre herramientas. Este código de notificación es idéntico a TTN \_ GETDISPINFO. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150534"
---
# <a name="ttn_needtext-notification-code"></a>Código de notificación de NEEDTEXT de TTN \_

Lo envía un control ToolTip para recuperar la información necesaria para mostrar una ventana de información sobre herramientas. Este código de notificación es idéntico a [TTN \_ GETDISPINFO](ttn-getdispinfo.md). Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) que identifica la herramienta que necesita texto y recibe la información solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para esta notificación.

## <a name="remarks"></a>Observaciones

Rellene los miembros adecuados de la estructura para devolver la información solicitada al control ToolTip. Si el controlador de mensajes establece el miembro **uFlags** de la estructura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) en ttf \_ di \_ SETITEM, el control ToolTip almacena la información y no la volverá a solicitar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TTN \_ NEEDTEXTW** (Unicode) y **TTN \_ NEEDTEXTA** (ANSI)<br/>                 |



 

 





