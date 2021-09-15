---
title: WM_POINTERDEVICECHANGE mensaje
description: Se envía a una ventana cuando hay un cambio en la configuración de un monitor que tiene asociado un digitalizador. Este mensaje contiene información sobre el escalado del modo de presentación.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- WM_POINTERDEVICECHANGE mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERDEVICECHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 38f570059f374f64e393e960a8458e605983d6c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569521"
---
# <a name="wm_pointerdevicechange-message"></a>WM_POINTERDEVICECHANGE mensaje

Se envía a una ventana cuando hay un cambio en la configuración de un monitor que tiene asociado un digitalizador. Este mensaje contiene información sobre el escalado del modo de presentación.

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no es compatible con PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no son compatibles con PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene un valor de [**Pointer Device Change Constants**](pointer-device-change-constants.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Información adicional específica del mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la aplicación procesa este mensaje, debe devolver cero.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes](messages.md)
</dt> </dl>

 

