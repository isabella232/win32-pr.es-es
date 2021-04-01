---
title: Código de notificación de LVN_ITEMACTIVATE (commctrl. h)
description: Lo envía un control de vista de lista cuando el usuario activa un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151281"
---
# <a name="lvn_itemactivate-notification-code"></a>Código de notificación de ITEMACTIVATE de LVN \_

Lo envía un control de vista de lista cuando el usuario activa un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versión 4,71](common-control-versions.md). Puntero a una estructura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contiene información sobre este código de notificación.

[Versión 4,70](common-control-versions.md) y versiones anteriores. Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que recibe este código de notificación debe devolver cero.

## <a name="remarks"></a>Observaciones

Para obtener los elementos que se van a activar, la aplicación receptora debe usar el mensaje [**LVM \_ GETSELECTEDCOUNT**](lvm-getselectedcount.md) para recuperar el número de elementos que se seleccionan y, a continuación, enviar el mensaje [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) con **LVNI \_ seleccionado** hasta que se hayan recuperado todos los elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





