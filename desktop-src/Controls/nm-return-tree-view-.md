---
title: Código de notificación de NM_RETURN (vista de árbol) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que el control tiene el foco de entrada y que el usuario ha presionado la tecla. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e4a048ec-4643-458a-bf75-f5b08163d6c6
keywords:
- Código de notificación de NM_RETURN (vista de árbol) controles de Windows
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0abf3152a9236103301f1c74acfcac69d43f07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996815"
---
# <a name="nm_return-tree-view-notification-code"></a>Código de notificación de retorno de NM \_ (vista de árbol)

Notifica a la ventana primaria de un control de vista de árbol que el control tiene el foco de entrada y que el usuario ha presionado la tecla. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_RETURN

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para evitar el procesamiento predeterminado o cero para permitir el procesamiento predeterminado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





