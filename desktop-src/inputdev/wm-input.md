---
title: WM_INPUT mensaje (Winuser.h)
description: Se envía a la ventana en la que se está obteniendo la entrada sin procesar. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- WM_INPUT entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468820"
---
# <a name="wm_input-message"></a>Mensaje \_ DE ENTRADA DE WM

Se envía a la ventana en la que se está obteniendo la entrada sin procesar.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam*

</dt> <dd>

Código de entrada. Use la macro [**GET \_ RAWINPUT \_ CODE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) para obtener el valor.

Puede ser uno de los siguientes valores:

| Value | Significado |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**BORDE \_ ENTRADA**</dt> <dt>0</dt> </dl> | La entrada se produjo mientras la aplicación estaba en primer plano. </br> La aplicación debe llamar [**a DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) que el sistema pueda realizar la limpieza. |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**BORDE \_ INPUTSINK**</dt> <dt>1</dt> </dl> | La entrada se produjo mientras la aplicación no estaba en primer plano. |

</dd> <dt>

*lParam* 

</dt> <dd>

Un **identificador HRAWINPUT** para la [**estructura RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) que contiene la entrada sin procesar del dispositivo. Para obtener los datos sin procesar, use este identificador en la llamada a [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

La entrada sin procesar solo está disponible cuando la aplicación llama [**a RegisterRawInputDevices con**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) especificaciones de dispositivo válidas.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Windows XP \[ solo aplicaciones de escritorio\] |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\] |
| Encabezado | <dl> <dt>**Winuser.h (incluir Windows.h)**</dt> </dl> |

## <a name="see-also"></a>Vea también

**Referencia**

[**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**GET \_ RAWINPUT \_ CODE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Conceptual**

[Entrada sin formato](raw-input.md)
