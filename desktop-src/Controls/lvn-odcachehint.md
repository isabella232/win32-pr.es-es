---
title: Código de notificación de LVN_ODCACHEHINT (commctrl. h)
description: Lo envía un control de vista de lista virtual cuando cambia el contenido de su área de presentación.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997182"
---
# <a name="lvn_odcachehint-notification-code"></a>Código de notificación de ODCACHEHINT de LVN \_

Lo envía un control de vista de lista virtual cuando cambia el contenido de su área de presentación. Por ejemplo, un control de vista de lista envía este código de notificación cuando el usuario desplaza la pantalla del control. El \_ código de notificación ODCACHEHINT de LVN se envía en forma de mensaje de notificación de [**WM \_**](wm-notify.md) .


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) que contiene información sobre el intervalo de elementos que se va a almacenar en caché.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que recibe este código de notificación debe devolver cero.

## <a name="remarks"></a>Observaciones

El control de este mensaje permite que la aplicación actualice la información del elemento que se mantiene en la memoria caché para que esté disponible fácilmente cuando se envíe un código de notificación [ \_ GETDISPINFO de LVN](lvn-getdispinfo.md) .

Tenga en cuenta que este código de notificación no siempre es una representación exacta de los elementos que [LVN \_ GETDISPINFO](lvn-getdispinfo.md)solicitará. Por lo tanto, si el elemento solicitado no se almacena en la memoria caché mientras se controla LVN \_ GETDISPINFO, la aplicación debe estar preparada para proporcionar la información solicitada de un origen fuera de la caché.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





