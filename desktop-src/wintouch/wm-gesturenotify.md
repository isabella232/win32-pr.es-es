---
title: Mensaje de WM_GESTURENOTIFY (Winuser. h)
description: Le ofrece la posibilidad de establecer la configuración de gestos.
ms.assetid: 83c23928-86ce-421d-bb84-5c41a770bf60
keywords:
- Mensaje de WM_GESTURENOTIFY de Windows Touch
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
ms.openlocfilehash: 5e900e4b607760df16938080a49f97a3ab0cf2ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150569"
---
# <a name="wm_gesturenotify-message"></a>Mensaje de GESTURENOTIFY de WM \_

Le ofrece la posibilidad de establecer la configuración de gestos.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sin usar.

</dd> <dt>

*lParam* 
</dt> <dd>

Un puntero a un [**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se debe devolver un valor de [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

Cuando se recibe el mensaje de **\_ GESTURENOTIFY de WM** , la aplicación puede usar [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) para especificar los gestos que se van a recibir. Este mensaje se debe propagar siempre mediante la función [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .

> [!Note]  
> Al controlar el mensaje de **\_ GESTURENOTIFY de WM** , se cambiará la configuración de gestos para la duración de la ventana, no solo para el gesto siguiente.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo habilitar todos los gestos. Para obtener más ejemplos, vea [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig).


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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[Guía de programación de gestos táctiles de Windows](guide-multi-touch-gestures.md)
</dt> <dt>

[**GESTURENOTIFYSTRUCT**](/windows/win32/api/winuser/ns-winuser-gesturenotifystruct)
</dt> <dt>

[**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig)
</dt> </dl>

 

