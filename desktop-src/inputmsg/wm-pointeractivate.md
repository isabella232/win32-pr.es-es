---
title: WM_POINTERACTIVATE mensaje
description: Se envía a una ventana inactiva cuando un puntero principal genera un WM_POINTERDOWN sobre la ventana.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_POINTERACTIVATE mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- WM_POINTERACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: b9bda11b5cb7a27f7744df6e20890a125a66bd88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569525"
---
# <a name="wm_pointeractivate-message"></a>WM_POINTERACTIVATE mensaje

Se envía a una ventana inactiva cuando un puntero principal genera un [**WM_POINTERDOWN**](wm-pointerdown.md) sobre la ventana. Siempre que el mensaje no se controle, se desplaza hacia arriba por la cadena de ventanas primarias hasta que llega a la ventana de nivel superior. Las aplicaciones pueden responder a este mensaje para especificar si desean activarse.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el identificador de puntero y la información adicional. Use las macros siguientes para recuperar esta información.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de puntero

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): valor de prueba de éxito devuelto al procesar el [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene el identificador de la ventana de nivel superior de la ventana que se está activando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver uno de los valores descritos en la sección Comentarios.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

Una aplicación puede controlar este mensaje y devolver uno de los siguientes valores para determinar cómo procesa el sistema la activación y la entrada de activación:

-   PA_ACTIVATE
-   PA_NOACTIVATE

Es importante tener en cuenta que, cuando el usuario interactúa con el sistema con varios punteros simultáneos, la oportunidad de activación que representa el mensaje WM_POINTERACTIVATE solo está **disponible para** las aplicaciones para el primero de esos punteros. Por lo tanto, las aplicaciones deben ser conscientes de que todavía pueden recibir entradas de punteros mientras están inactivas.

Si la aplicación no controla este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) pasa el mensaje a la ventana primaria.

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

 

