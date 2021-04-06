---
title: Código de notificación de NM_KEYDOWN (barra de herramientas) (commctrl. h)
description: Se envía por un control cuando el control tiene el foco de teclado y el usuario presiona una tecla. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- Código de notificación de NM_KEYDOWN (barra de herramientas) controles de Windows
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7326946a8234122c81b2fd057dab0ad313d49a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078858"
---
# <a name="nm_keydown-toolbar-notification-code"></a>NM \_ código de notificación de KEYDOWN (Toolbar)

Se envía por un control cuando el control tiene el foco de teclado y el usuario presiona una tecla. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contiene información adicional sobre la clave que produjo el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para evitar que el control procese la clave o cero de lo contrario.

## <a name="remarks"></a>Observaciones

Actualmente, solo el control de barra de herramientas envía este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





