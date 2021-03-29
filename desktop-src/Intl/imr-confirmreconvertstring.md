---
description: Notifica a una aplicación cuando el IME debe cambiar la estructura RECONVERTSTRING. La aplicación recibe este comando a través del \_ mensaje de solicitud del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: Código de notificación de IMR_CONFIRMRECONVERTSTRING (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813683"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>Código de notificación de IMR \_ CONFIRMRECONVERTSTRING

Notifica a una aplicación cuando el IME debe cambiar la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) . La aplicación recibe este comando a través del mensaje de [**\_ \_ solicitud del IME de WM**](wm-ime-request.md) con la configuración de parámetros, como se muestra a continuación.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMR \_ CONFIRMRECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a una estructura de [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) desde el IME. Para obtener más información, vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si la aplicación acepta la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) modificada. De lo contrario, el comando devuelve 0 y el IME usa la estructura **RECONVERTSTRING** original.

## <a name="remarks"></a>Observaciones

La aplicación rellena la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) al recibir el comando [IMR \_ RECONVERTSTRING](imr-reconvertstring.md) .

Una vez que la aplicación ha controlado una [IMR \_ RECONVERTSTRING](imr-reconvertstring.md), el IME podría o no ajustar la estructura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) . El IME envía una \_ solicitud del IME \_ de WM con **IMR \_ CONFIRMRECONVERTSTRING** para confirmar los cambios en la estructura **RECONVERTSTRING** . Si la aplicación devuelve **true** para **IMR \_ CONFIRMRECONVERTSTRING**, el IME genera una nueva cadena de composición basada en la estructura **RECONVERTSTRING** para el comando **IMR \_ CONFIRMRECONVERTSTRING** . Si la aplicación devuelve **false** para **IMR \_ CONFIRMRECONVERTSTRING**, el IME genera una nueva cadena de composición basada en la estructura **RECONVERTSTRING** original especificada por la aplicación en el \_ comando IMR RECONVERTSTRING.

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

[IMR \_ RECONVERTSTRING](imr-reconvertstring.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_solicitud de IME de WM \_**](wm-ime-request.md)
</dt> </dl>

 

 




