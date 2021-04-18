---
description: Notifica a una aplicación cuando un IME está a punto de cerrar la ventana candidatos. La aplicación recibe este comando a través del \_ mensaje de notificación del IME \_ de WM con la configuración de parámetros, como se muestra a continuación.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: Código de notificación de IMN_CLOSECANDIDATE (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3414d2aa37a50b7f35f0dfb936b641b7c86a932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687618"
---
# <a name="imn_closecandidate-notification-code"></a>Código de notificación de CLOSECANDIDATE de IMN \_

Notifica a una aplicación cuando un IME está a punto de cerrar la ventana candidatos. La aplicación recibe este comando a través del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establézcalo en IMN \_ CLOSECANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Marca de lista de candidatos. Cada bit corresponde a una lista de candidatos: bit 0 a la primera lista, bit 1 a segundo, etc. Si un bit especificado es 1, la ventana candidata correspondiente está a punto de cerrarse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación debe procesar este comando si muestra los propios candidatos.

De forma predeterminada, la ventana del IME destruye una ventana candidata al procesar este comando.

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

 

 




