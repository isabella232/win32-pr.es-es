---
description: Notifica a una aplicación cuando un IME está a punto de mostrar un mensaje de error u otra información. La aplicación recibe este comando a través del mensaje WM \_ IME \_ NOTIFY con la configuración de parámetros, como se muestra a continuación.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: IMN_GUIDELINE de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8bbcce8c1e7a04f4474d09f221ff2e2644e84b49d98edf09c1137604b71b226
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107105"
---
# <a name="imn_guideline-notification-code"></a>Código de notificación DE LA GUÍA DE IMN \_

Notifica a una aplicación cuando un IME está a punto de mostrar un mensaje de error u otra información. La aplicación recibe este comando a través del mensaje [**\_ WM IME \_ NOTIFY**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMN \_ GUIDELINE (GUÍA DE IMN).

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

Una aplicación procesa este comando llamando a la función [**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) para recuperar el mensaje de error o la información del IME.

La ventana IME muestra el mensaje de error o la cadena de información en una ventana de información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos del Administrador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




