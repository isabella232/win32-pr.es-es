---
title: Código de notificación de LVN_ITEMCHANGED (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que un elemento ha cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED controles de código de notificación de Windows
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
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658418"
---
# <a name="lvn_itemchanged-notification-code"></a>Código de notificación de LVN \_ ITEMCHANGED

Notifica a la ventana primaria de un control de vista de lista que un elemento ha cambiado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que identifica el elemento y especifica cuál de sus atributos ha cambiado. Si el miembro **iItem** de la estructura a la que apunta *lParam* es-1, el cambio se ha aplicado a todos los elementos de la vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si un control de vista de lista tiene el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) y el usuario selecciona un intervalo de elementos manteniendo presionada la tecla Mayús y haciendo clic en el mouse, \_ no se enviarán los códigos de notificación LVN ITEMCHANGED para cada elemento seleccionado o no seleccionado. En su lugar, recibirá un solo código de notificación [ \_ ODSTATECHANGED de LVN](lvn-odstatechanged.md) , que indica que un intervalo de elementos ha cambiado de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





