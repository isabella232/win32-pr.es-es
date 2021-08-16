---
title: LVN_ITEMCHANGED de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que un elemento ha cambiado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea129a1b62b442b0fb545f29a57e9eab0d6d1bae057996df5bc269d9a4296d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830389"
---
# <a name="lvn_itemchanged-notification-code"></a>Código de notificación ITEMCHANGED de LVN \_

Notifica a la ventana primaria de un control de vista de lista que un elemento ha cambiado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que identifica el elemento y especifica cuál de sus atributos ha cambiado. Si el **miembro iItem** de la estructura a la que *apunta lParam* es -1, el cambio se ha aplicado a todos los elementos de la vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si un control de vista de lista tiene el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) y el usuario selecciona un intervalo de elementos manteniendo presionada la tecla MAYÚS y haciendo clic en el mouse, los códigos de notificación LVN ITEMCHANGED no se envían para cada elemento seleccionado o \_ deseleccionado. En su lugar, recibirá un único código de [notificación LVN \_ ODSTATECHANGED,](lvn-odstatechanged.md) que indica que un intervalo de elementos ha cambiado de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





