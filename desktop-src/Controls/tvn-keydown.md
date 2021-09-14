---
title: TVN_KEYDOWN de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que el usuario ha presionado una tecla y el control de vista de árbol tiene el foco de entrada. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165541"
---
# <a name="tvn_keydown-notification-code"></a>Código de notificación \_ DE TVN KEYDOWN

Notifica a la ventana primaria de un control de vista de árbol que el usuario ha presionado una tecla y el control de vista de árbol tiene el foco de entrada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVKEYDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) El **miembro wVKey** especifica el código de clave virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el **miembro wVKey** de *lParam* es un código de clave de caracteres, el carácter se usará como parte de una búsqueda incremental. Devuelve distinto de cero para excluir el carácter de la búsqueda incremental o cero para incluir el carácter en la búsqueda. Para todas las demás claves, se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





