---
title: LVN_ITEMACTIVATE de notificación (Commctrl.h)
description: Enviado por un control list-view cuando el usuario activa un elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE código de notificación Windows controles
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
ms.openlocfilehash: f21b02406157a13d2fcf110c15e692211b26b3f9da31741489e317e6b2c68309
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105055"
---
# <a name="lvn_itemactivate-notification-code"></a>Código de notificación \_ LVN ITEMACTIVATE

Enviado por un control list-view cuando el usuario activa un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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

[Versión 4.71.](common-control-versions.md) Puntero a una [**estructura NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contiene información sobre este código de notificación.

[Versión 4.70](common-control-versions.md) y anteriores. Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que recibe este código de notificación debe devolver cero.

## <a name="remarks"></a>Comentarios

Para obtener los elementos que se activan, la aplicación receptora debe usar el mensaje [**LVM \_ GETSELECTEDCOUNT**](lvm-getselectedcount.md) para recuperar el número de elementos seleccionados y, a continuación, enviar el mensaje [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) con **LVNI \_ SELECTED** hasta que se hayan recuperado todos los elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





