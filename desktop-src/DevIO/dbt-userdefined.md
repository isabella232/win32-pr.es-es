---
description: El \_ evento DBT USERDEFINED Device identifica un evento definido por el usuario.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: Evento DBT_USERDEFINED (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080195"
---
# <a name="dbt_userdefined-event"></a>\_Evento USERDEFINED DBT

El \_ evento DBT USERDEFINED Device identifica un evento definido por el usuario.

Para difundir este evento de dispositivo, llame a la función [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) con el mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) . Establezca *wParam* en DBT \_ USERDEFINED y establezca *lParam* como se describe a continuación.


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*identificador* 
</dt> <dd>

Identificador a una ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador del mensaje de [**\_ DEVICECHANGE de WM**](wm-devicechange.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Establezca en DBT \_ USERDEFINED.

</dd> <dt>

*lParam* 
</dt> <dd>

Un puntero a una estructura [**\_ \_ \_ USERDEFINED de difusión de desarrollo**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) que describe la difusión definida por el usuario en curso. El miembro **dbud \_ szName** contiene el nombre del mensaje definido por el usuario, seguido de los datos definidos por el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>DBT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Eventos de administración de dispositivos](device-management-events.md)
</dt> <dt>

[**\_DESARROLLO de \_ difusión \_ USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**DEVICECHANGE de WM \_**](wm-devicechange.md)
</dt> <dt>

[**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

