---
description: Notifica a una aplicación cuando se actualiza el estado abierto del contexto de entrada. La aplicación recibe este comando a través del mensaje WM \_ IME \_ NOTIFY con la configuración de parámetros, como se muestra a continuación.
ms.assetid: cc6fa7f4-b85a-486a-985d-53c071321bd1
title: IMN_SETOPENSTATUS de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57797210f9c0595a952315ca75858890b1998fe16e49049b3a22fb8ed72a5aea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107045"
---
# <a name="imn_setopenstatus-notification-code"></a>Código de notificación \_ SETOPENSTATUS de IMN

Notifica a una aplicación cuando se actualiza el estado abierto del contexto de entrada. La aplicación recibe este comando a través del mensaje [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_SETOPENSTATUS
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMN \_ SETOPENSTATUS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

La aplicación puede obtener información sobre el estado de apertura mediante la [**función ImmGetOpenStatus.**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)

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

[**ImmGetOpenStatus**](/windows/desktop/api/Imm/nf-imm-immgetopenstatus)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




