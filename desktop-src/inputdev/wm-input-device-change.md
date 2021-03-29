---
title: Mensaje de WM_INPUT_DEVICE_CHANGE (Winuser. h)
description: Se envía a la ventana que se registró para recibir entradas sin procesar. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- Entrada de mouse y teclado de mensaje de WM_INPUT_DEVICE_CHANGE
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
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "104078545"
---
# <a name="wm_input_device_change-message"></a>Mensaje WM_INPUT_DEVICE_CHANGE

## <a name="description"></a>Descripción

Se envía a la ventana que se registró para recibir entradas sin procesar. 

Las notificaciones de entrada sin formato solo están disponibles después de que la aplicación llame a [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) con [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) marca.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam*

</dt> <dd>

Tipo: **wParam**

Este parámetro puede ser uno de los valores siguientes.

| Valor                    | Significado                                    |
|--------------------------|--------------------------------------------|
| **llegada de GIDC \_** </br>1 | Se ha agregado un nuevo dispositivo al sistema. </br> Puede llamar a [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) para obtener más información sobre el dispositivo. |
| **eliminación de GIDC \_** </br>2 | Se ha quitado un dispositivo del sistema. |

</dd> <dt>

*lParam* 

</dt> <dd>

Tipo: **lParam**

**Identificador** del dispositivo de entrada sin formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="see-also"></a>Vea también

**Vista**

[Entrada sin formato](/windows/desktop/inputdev/raw-input)

**Referencia**

[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[Estructura RAWINPUTDEVICE](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

