---
title: Mensaje de WM_INPUT (Winuser. h)
description: Se envía a la ventana que obtiene la entrada sin formato. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- Entrada de mouse y teclado de mensaje de WM_INPUT
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422194"
---
# <a name="wm_input-message"></a>Mensaje de entrada de WM \_

Se envía a la ventana que obtiene la entrada sin formato.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam*

</dt> <dd>

Código de entrada. Use la macro [**Get \_ RAWINPUT \_ code \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) para obtener el valor.

Puede ser uno de los siguientes valores:

| Value | Significado |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**RIM \_ ENTRADA**</dt> <dt>0</dt> </dl> | La entrada se produjo mientras la aplicación estaba en primer plano. </br> La aplicación debe llamar a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que el sistema pueda realizar la limpieza. |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**RIM \_ INPUTSINK**</dt> <dt>1</dt> </dl> | La entrada se produjo mientras la aplicación no estaba en primer plano. |

</dd> <dt>

*lParam* 

</dt> <dd>

Identificador de **HRAWINPUT** de la estructura [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) que contiene la entrada sin formato del dispositivo. Para obtener los datos sin procesar, use este identificador en la llamada a [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

La entrada sin formato solo está disponible cuando la aplicación llama a [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) con especificaciones de dispositivo válidas.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows XP \[\] |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2003 \[\] |
| Encabezado | <dl> <dt>**Winuser. h (incluir Windows. h)**</dt> </dl> |

## <a name="see-also"></a>Vea también

**Referencia**

[**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**OBTENCIÓN \_ del \_ código RAWINPUT \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Vista**

[Entrada sin formato](raw-input.md)
