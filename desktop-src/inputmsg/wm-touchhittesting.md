---
title: WM_TOUCHHITTESTING mensaje
description: Se envía a una ventana en un menú táctil para determinar el destino táctil más probable.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- WM_TOUCHHITTESTING mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569477"
---
# <a name="wm_touchhittesting-message"></a>WM_TOUCHHITTESTING mensaje

Se envía a una ventana en un menú táctil para determinar el destino táctil más probable.

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no tiene reconocimiento de PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no tienen reconocimiento de PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sin usar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) que contiene los datos del área de contacto táctil.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si uno o varios elementos están dentro del área de contacto táctil, una aplicación debe devolver el resultado [**de PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).

Si no hay elementos dentro del área de contacto  táctil, una aplicación debe establecer el valor de puntuación en [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) en TOUCH_HIT_TESTING_PROXIMITY_FARTHEST y llamar [**a**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) para obtener el valor devuelto LRESULT.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

Este mensaje se envía a las ventanas que se registran a [**través de la función RegisterTouchHitTestingWindow.**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Mensajes](messages.md)
</dt> <dt>

[**Puntuaciones de pruebas de impacto táctil**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

