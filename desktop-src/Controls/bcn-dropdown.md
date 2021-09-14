---
title: BCN_DROPDOWN de notificación (Winuser.h)
description: Se envía cuando el usuario hace clic en una flecha desplegable de un botón. La ventana primaria del control recibe este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968731"
---
# <a name="bcn_dropdown-notification-code"></a>Código de notificación \_ DE BCN DROPDOWN

Se envía cuando el usuario hace clic en una flecha desplegable de un botón. La ventana primaria del control recibe este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMBCDROPDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) El **miembro rcButton** se establece para describir el área desplegable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte **LPARAM** para recuperar la [**estructura NMBCDROPDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) **WPARAM** contiene el identificador del control que envía este mensaje. El control de botón debe tener un estilo de botón desplegable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





