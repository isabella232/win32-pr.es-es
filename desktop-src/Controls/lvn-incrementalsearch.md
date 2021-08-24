---
title: LVN_INCREMENTALSEARCH de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que se ha iniciado una búsqueda incremental. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec3207fbb16bca23bf44ac61fee58bb6e4fad1ff74c38d7b56910ed52997f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826125"
---
# <a name="lvn_incrementalsearch-notification-code"></a>Código de notificación \_ DE LVN INCREMENTALSEARCH

Notifica a la ventana primaria de un control de vista de lista que se ha iniciado una búsqueda incremental. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una [**estructura NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que describe el código de notificación. El autor de la llamada es responsable de asignar esta estructura, incluidas las estructuras [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) y [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenidas. Establezca los miembros de la **estructura NMHDR.** El **miembro** de código debe establecerse en LVN \_ INCREMENTALSEARCH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El receptor de notificaciones convierte *lParam* para recuperar la [**estructura NMLVFINDITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) El *parámetro wParam* contiene el identificador del control que envía este código de notificación.

Este código de notificación ofrece a una aplicación (o al receptor de notificaciones) la oportunidad de personalizar una búsqueda incremental. Por ejemplo, si los elementos de búsqueda son numéricos, la aplicación puede realizar una búsqueda numérica en lugar de una búsqueda de cadenas.

La aplicación establece el miembro **lParam** de la estructura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenida en la estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) en el resultado de la búsqueda o en otro valor definido por la aplicación para producir un error en la búsqueda e indicar al control cómo continuar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl>   |
| Nombres Unicode y ANSI<br/>   | **LVN \_ INCREMENTALSEARCHW** (Unicode) y **LVN \_ INCREMENTALSEARCHA** (ANSI)<br/> |



 

 





