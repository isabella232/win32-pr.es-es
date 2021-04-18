---
description: Notifica a una aplicación cuando un IME está a punto de crear la ventana de estado. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: Código de notificación de IMN_OPENSTATUSWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca33771d1474c2f2ac78551a31545cecc2e513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687615"
---
# <a name="imn_openstatuswindow-notification-code"></a>Código de notificación de OPENSTATUSWINDOW de IMN \_

Notifica a una aplicación cuando un IME está a punto de crear la ventana de estado. La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establézcalo en IMN \_ OPENSTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación procesa este comando para mostrar la ventana de estado para el IME.

La ventana del IME crea una ventana de estado al procesar este comando y establece las cadenas que se van a mostrar en la ventana en el contexto de entrada. Las aplicaciones pueden obtener información sobre la ventana de estado mediante la función [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) .

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

[**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**\_notificación de IME de WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




