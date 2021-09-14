---
title: NM_RDBLCLK de notificación (vista de árbol) (Commctrl.h)
description: Notifica al elemento primario de un control de vista de árbol que el usuario ha hecho doble clic en el botón derecho del mouse dentro del control. Esta notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- NM_RDBLCLK (vista de árbol) código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5b4f1dbaf1031c995028028cc0b44e544f5f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167909"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a>Código \_ de notificación DE NM RDBLCLK (vista de árbol)

Notifica al elemento primario de un control de vista de árbol que el usuario ha hecho doble clic en el botón derecho del mouse dentro del control. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RDBLCLK

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



 

 





