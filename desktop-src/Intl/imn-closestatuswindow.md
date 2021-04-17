---
description: Notifica a una aplicación cuando un IME está a punto de cerrar la ventana de estado. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: Código de notificación de IMN_CLOSESTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0347fb4b0d83a9e3891b9aea59d82ab81e2183
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652706"
---
# <a name="imn_closestatuswindow-notification-code"></a>Código de notificación de CLOSESTATUSWINDOW de IMN \_

Notifica a una aplicación cuando un IME está a punto de cerrar la ventana de estado. La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establézcalo en IMN \_ CLOSESTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este comando si muestra la ventana de estado para el IME.

La ventana del IME cierra la ventana de estado al procesar este comando.

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

[**\_notificación de IME de WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




