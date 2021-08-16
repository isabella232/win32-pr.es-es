---
title: LVN_ENDSCROLL mensaje (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista cuando finaliza una operación de desplazamiento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- LVN_ENDSCROLL controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d0abc3c12170dbc14f5e8a67329ed226610baa7b00fd042a24ed67193e6df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915145"
---
# <a name="lvn_endscroll-message"></a>Mensaje \_ ENDSCROLL de LVN

Notifica a la ventana primaria de un control de vista de lista cuando finaliza una operación de desplazamiento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) que contiene la posición horizontal o vertical de donde finaliza la operación de desplazamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor devuelto no utilizado.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





