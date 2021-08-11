---
title: WM_INPUT_DEVICE_CHANGE mensaje (Winuser.h)
description: Se envía a la ventana que se registró para recibir la entrada sin procesar. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823aeaf5655703802f07fb238d5c6c5dc479defa12ae4a416423b4519fd2b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247891"
---
# <a name="wm_input_device_change-message"></a>WM_INPUT_DEVICE_CHANGE mensaje

## <a name="description"></a>Descripción

Se envía a la ventana que se registró para recibir la entrada sin procesar. 

Las notificaciones de entrada sin procesar solo están disponibles después de que la aplicación llame a [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) marca.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam*

</dt> <dd>

Tipo: **WPARAM**

Este parámetro puede ser uno de los valores siguientes.

| Valor                    | Significado                                    |
|--------------------------|--------------------------------------------|
| **LLEGADA DE \_ GIDC** </br>1 | Se ha agregado un nuevo dispositivo al sistema. </br> Puede llamar a [GetRawInputDeviceInfo para](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) obtener más información sobre el dispositivo. |
| **ELIMINACIÓN DE \_ GIDC** </br>2 | Se ha quitado un dispositivo del sistema. |

</dd> <dt>

*lParam* 

</dt> <dd>

Tipo: **LPARAM**

Identificador **del** dispositivo de entrada sin procesar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="see-also"></a>Consulte también

**Conceptual**

[Entrada sin procesar](/windows/desktop/inputdev/raw-input)

**Referencia**

[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[RawINPUTDEVICE (estructura)](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

