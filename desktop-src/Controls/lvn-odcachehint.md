---
title: LVN_ODCACHEHINT de notificación (Commctrl.h)
description: Enviado por un control de vista de lista virtual cuando el contenido de su área de presentación ha cambiado.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072303"
---
# <a name="lvn_odcachehint-notification-code"></a>Código de notificación de LVN \_ ODCACHEHINT

Enviado por un control de vista de lista virtual cuando el contenido de su área de presentación ha cambiado. Por ejemplo, un control de vista de lista envía este código de notificación cuando el usuario desplaza la presentación del control. El código de notificación \_ LVN ODCACHEHINT se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) que contiene información sobre el intervalo de elementos que se almacenarán en caché.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que recibe este código de notificación debe devolver cero.

## <a name="remarks"></a>Observaciones

El control de este mensaje permite a la aplicación actualizar la información del elemento que se mantiene en caché para que esté disponible fácilmente cuando se envía un código de [notificación \_ LVN GETDISPINFO.](lvn-getdispinfo.md)

Tenga en cuenta que este código de notificación no siempre es una representación exacta de los elementos solicitados por [LVN \_ GETDISPINFO](lvn-getdispinfo.md). Por lo tanto, si el elemento solicitado no se almacena en caché mientras se administra LVN GETDISPINFO, la aplicación debe estar preparada para proporcionar la información solicitada desde un origen \_ fuera de la memoria caché.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





