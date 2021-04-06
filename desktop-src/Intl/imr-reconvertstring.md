---
description: Notifica a una aplicación cuando un IME seleccionado necesita una cadena para la reconversión. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: Código de notificación de IMR_RECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909501"
---
# <a name="imr_reconvertstring-notification-code"></a>Código de notificación de IMR \_ RECONVERTSTRING

Notifica a una aplicación cuando un IME seleccionado necesita una cadena para la reconversión. La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMR \_ RECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a un búfer que contiene la estructura y las cadenas de [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la estructura de la cadena de reconversión actual. Si *lParam* se establece en **null**, la aplicación devuelve el tamaño del búfer necesario para contener la estructura. El comando devuelve 0 si no se realiza correctamente.

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

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_solicitud de IME de WM \_**](wm-ime-request.md)
</dt> </dl>

 

 




