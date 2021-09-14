---
description: El evento de dispositivo \_ DBT USERDEFINED identifica un evento definido por el usuario.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: DBT_USERDEFINED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164442"
---
# <a name="dbt_userdefined-event"></a>Evento \_ DEFINIDO por el usuario de DBT

El evento de dispositivo \_ DBT USERDEFINED identifica un evento definido por el usuario.

Para difundir este evento de dispositivo, llame a [**la función BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) con el [**mensaje \_ DEVICECHANGE de WM.**](wm-devicechange.md) Establezca *wParam en* DBT \_ USERDEFINED y establezca *lParam* como se describe a continuación.


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador a una ventana.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador [**del mensaje \_ DEVICECHANGE**](wm-devicechange.md) de WM.

</dd> <dt>

*wParam* 
</dt> <dd>

Se establece en DBT \_ USERDEFINED.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**\_ \_ DEV BROADCAST \_ USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) que describe la difusión definida por el usuario en curso. El **miembro dbud \_ szName** contiene el nombre del mensaje definido por el usuario, seguido de los datos definidos por el usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2003<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Administración de dispositivos eventos](device-management-events.md)
</dt> <dt>

[**\_DIFUSIÓN DE DESARROLLO \_ \_ DEFINIDA POR EL USUARIO**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> <dt>

[**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

