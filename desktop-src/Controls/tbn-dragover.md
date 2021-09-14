---
title: TBN_DRAGOVER de notificación (Commctrl.h)
description: Determina si se debe enviar un mensaje MARKBUTTON de \_ TB para un botón que se está arrastrando. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166377"
---
# <a name="tbn_dragover-notification-code"></a>Código de notificación DRAGOVER de TBN \_

Determina si se debe [**enviar un \_ mensaje MARKBUTTON**](tb-markbutton.md) de TB para un botón que se está arrastrando. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que especifica qué elemento se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**FALSE** si la barra de herramientas debe enviar un mensaje \_ MARKBUTTON de TB; de lo **contrario, TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





