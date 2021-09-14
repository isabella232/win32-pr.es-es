---
title: NM_RCLICK (vista de árbol) (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que el usuario ha hecho clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 5816d8b8-7f3d-477d-9116-1b3670d99240
keywords:
- NM_RCLICK (vista de árbol) código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d72ee220bf33189e8954a2e1ef454b22886553
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167933"
---
# <a name="nm_rclick-tree-view-notification-code"></a>Código de notificación de NM \_ RCLICK (vista de árbol)

Notifica a la ventana primaria de un control de vista de árbol que el usuario ha hecho clic en el botón derecho del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para evitar el procesamiento predeterminado o cero para permitir el procesamiento predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





