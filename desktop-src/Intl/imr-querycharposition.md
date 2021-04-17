---
description: Notifica a una aplicación cuando el IME seleccionado necesita información sobre las coordenadas de un carácter en la cadena de composición. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: Código de notificación de IMR_QUERYCHARPOSITION (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687455"
---
# <a name="imr_querycharposition-notification-code"></a>Código de notificación de IMR \_ QUERYCHARPOSITION

Notifica a una aplicación cuando el IME seleccionado necesita información sobre las coordenadas de un carácter en la cadena de composición. La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMR \_ QUERYCHARPOSITION.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a una estructura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) que contiene la posición del carácter en la ventana de composición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la aplicación rellena la estructura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) . De lo contrario, el comando devuelve 0.

## <a name="remarks"></a>Observaciones

Una aplicación que dibuja la propia cadena de composición, en lugar de depender del IME, es responsable de rellenar todos los miembros de la estructura [**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition) . De lo contrario, la aplicación debe pasar el comando a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) si tiene su propia ventana de interfaz de usuario de IME.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**IMECHARPOSITION**](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[**\_solicitud de IME de WM \_**](wm-ime-request.md)
</dt> </dl>

 

 
