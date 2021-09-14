---
title: LVN_ODFINDITEM mensaje (Commctrl.h)
description: Enviado por un control de vista de lista virtual cuando necesita que el propietario encuentre un elemento de devolución de llamada determinado.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- LVN_ODFINDITEM controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362571"
---
# <a name="lvn_odfinditem-message"></a>Mensaje \_ ODFINDITEM de LVN

Enviado por un control [de vista de lista](list-view-controls-overview.md) virtual cuando necesita que el propietario encuentre un elemento de devolución de llamada determinado. Por ejemplo, el control enviará este código de notificación cuando reciba una entrada de teclado de método abreviado o cuando reciba un mensaje [**\_ LVM FINDITEM.**](lvm-finditem.md) El código de \_ notificación LVN ODFINDITEM se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que incluye información que se usará para la búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento encontrado o -1 si no se encuentra ningún elemento.

## <a name="remarks"></a>Observaciones

La información de búsqueda se envía en forma de una [**estructura LVFINDINFO,**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) que es miembro de la estructura [**NMLVFINDITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ ODFINDITEMW** (Unicode) y **LVN \_ ODFINDITEMA** (ANSI)<br/>             |



 

 





