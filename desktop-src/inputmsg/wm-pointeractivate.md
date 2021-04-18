---
title: Mensaje WM_POINTERACTIVATE
description: Se envía a una ventana inactiva cuando un puntero primario genera un WM_POINTERDOWN sobre la ventana.
ms.assetid: 4eec37da-227c-4be1-bf0b-99704caa1322
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERACTIVATE
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720220"
---
# <a name="wm_pointeractivate-message"></a>Mensaje WM_POINTERACTIVATE

Se envía a una ventana inactiva cuando un puntero primario genera un [**WM_POINTERDOWN**](wm-pointerdown.md) sobre la ventana. Siempre que el mensaje permanezca no controlado, recorre la cadena de la ventana primaria hasta que llega a la ventana de nivel superior. Las aplicaciones pueden responder a este mensaje para especificar si desean que se activen.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_POINTERACTIVATE             0x024B
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene el identificador de puntero e información adicional. Use las siguientes macros para recuperar esta información.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): identificador de puntero

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): el valor de la prueba de posicionamiento devolvió el procesamiento del mensaje de [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene el identificador de la ventana de nivel superior de la ventana que se está activando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver uno de los valores descritos en la sección Comentarios.

Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Observaciones

Una aplicación puede controlar este mensaje y devolver uno de los valores siguientes para determinar la forma en que el sistema procesa la activación y la entrada de activación:

-   PA_ACTIVATE
-   PA_NOACTIVATE

Es importante tener en cuenta que, cuando el usuario interactúa con el sistema con varios punteros simultáneos, la oportunidad de activación que el mensaje de **WM_POINTERACTIVATE** representa está disponible para las aplicaciones solo para el primero de esos punteros. Por lo tanto, las aplicaciones deben tener en cuenta que pueden seguir recibiendo entradas de punteros mientras están inactivas.

Si la aplicación no controla este mensaje, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) pasa el mensaje a la ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes](messages.md)
</dt> </dl>

 

