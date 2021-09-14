---
description: Notifica a una aplicación cuando se actualiza el estilo o la posición de la ventana de composición. La aplicación recibe este comando a través del mensaje \_ WM IME \_ NOTIFY con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: IMN_SETCOMPOSITIONWINDOW de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a1a4e989fb36049168359f86f85ee7a58103a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063113"
---
# <a name="imn_setcompositionwindow-notification-code"></a>Código de notificación \_ DE IMN SETCOMPOSITIONWINDOW

Notifica a una aplicación cuando se actualiza el estilo o la posición de la ventana de composición. La aplicación recibe este comando a través del mensaje [**\_ WM IME \_ NOTIFY**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMN \_ SETCOMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

La aplicación puede obtener información sobre el formulario de composición mediante el comando [**\_ GETCOMPOSITIONWINDOW de IMC.**](imc-getcompositionwindow.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del Administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**IMC \_ GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




