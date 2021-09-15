---
title: WM_POINTERDEVICEINRANGE mensaje
description: Se envía a una ventana cuando se detecta un dispositivo de puntero dentro del intervalo de un digitalizador de entrada. Este mensaje contiene información sobre el dispositivo y su proximidad.
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- WM_POINTERDEVICEINRANGE mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 76ab6ac4f96d1df4e4e29afbcefe86d34b8b602d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569520"
---
# <a name="wm_pointerdeviceinrange-message"></a>WM_POINTERDEVICEINRANGE mensaje

Se envía a una ventana cuando se detecta un dispositivo de puntero dentro del intervalo de un digitalizador de entrada. Este mensaje contiene información sobre el dispositivo y su proximidad.

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no tiene reconocimiento de PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no tienen reconocimiento de PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Información adicional específica del mensaje.

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

 

