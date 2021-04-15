---
title: Código de notificación de TVN_KEYDOWN (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que el usuario presionó una tecla y el control de vista de árbol tiene el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489016"
---
# <a name="tvn_keydown-notification-code"></a>\_Código de notificación KEYDOWN de TVN

Notifica a la ventana primaria de un control de vista de árbol que el usuario presionó una tecla y el control de vista de árbol tiene el foco de entrada. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTVKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) . El miembro **wVKey** especifica el código de la clave virtual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el miembro **wVKey** de *lParam* es un código de tecla de carácter, el carácter se usará como parte de una búsqueda incremental. Devuelve un valor distinto de cero para excluir el carácter de la búsqueda incremental o cero para incluir el carácter en la búsqueda. Para todas las demás claves, se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





