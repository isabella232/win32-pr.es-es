---
title: Código de notificación de NM_SETCURSOR (vista de árbol) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que el control está estableciendo el cursor en respuesta a un mensaje de SETCURSOR de WM \_ . Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- Código de notificación de NM_SETCURSOR (vista de árbol) controles de Windows
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40b733e32c72abc9620e0fd18a6ef554aee9214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996814"
---
# <a name="nm_setcursor-tree-view-notification-code"></a>NM \_ SETCURSOR (vista de árbol) código de notificación

Notifica a la ventana primaria de un control de vista de árbol que el control está estableciendo el cursor en respuesta a un mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) . Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que el control establezca el cursor o un valor distinto de cero para evitar que el control establezca el cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

