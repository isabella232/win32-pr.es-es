---
title: WM_GESTURENOTIFY mensaje (Winuser.h)
description: Le ofrece la oportunidad de establecer la configuración de gestos.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- WM_GESTURENOTIFY mensaje Windows Touch
topic_type:
- apiref
api_name:
- WM_GESTURENOTIFY
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d474f356310a0d7949cecf36e7af9cb586a76029171dfe27c1679970e481ed1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435241"
---
# <a name="wm_gesturenotify-message"></a>WM \_ GESTURENOTIFY message

Le ofrece la oportunidad de establecer la configuración de gestos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sin usar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a [**una estructura GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se debe devolver un valor de [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Comentarios

Cuando se recibe el mensaje **\_ WM GESTURENOTIFY,** la aplicación puede usar [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) para especificar los gestos que se recibirán. Este mensaje siempre se debe burbujas con la [función DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca)

> [!Note]  
> El control **del mensaje \_ WM GESTURENOTIFY** cambiará la configuración del gesto durante la vigencia de la ventana, no solo para el siguiente gesto.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo habilitar todos los gestos. Para obtener más ejemplos, [**vea SetGestureConfig.**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)


```C++
    switch (message)
    {
    case WM_GESTURENOTIFY:
        GESTURECONFIG gc = {0,GC_ALLGESTURES,0};
        BOOL bResult = SetGestureConfig(hWnd,0,1,&gc,sizeof(GESTURECONFIG));
            
        if(!bResult)
        {
            // an error
        }
        return DefWindowProc(hWnd, WM_GESTURENOTIFY, wParam, lParam);
    }
      
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[Windows Guía de programación de gestos táctiles](guide-multi-touch-gestures.md)
</dt> <dt>

[**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

