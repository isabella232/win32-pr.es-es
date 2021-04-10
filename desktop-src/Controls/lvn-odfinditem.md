---
title: Mensaje de LVN_ODFINDITEM (commctrl. h)
description: Lo envía un control de vista de lista virtual cuando necesita que el propietario busque un elemento de devolución de llamada determinado.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- LVN_ODFINDITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150663"
---
# <a name="lvn_odfinditem-message"></a>LVN \_ ODFINDITEM

Lo envía un control [de vista de lista virtual](list-view-controls-overview.md) cuando necesita que el propietario busque un elemento de devolución de llamada determinado. Por ejemplo, el control enviará este código de notificación cuando reciba entradas de teclado de acceso directo o cuando reciba un mensaje de [**LVM de LVM \_**](lvm-finditem.md) . El \_ código de notificación ODFINDITEM de LVN se envía en forma de mensaje de notificación de [**WM \_**](wm-notify.md) .


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que incluye la información que se va a usar para la búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento encontrado o-1 si no se encuentra ningún elemento.

## <a name="remarks"></a>Observaciones

La información de búsqueda se envía en forma de una estructura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , que es un miembro de la estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ ODFINDITEMW** (Unicode) y **LVN \_ ODFINDITEMA** (ANSI)<br/>             |



 

 





