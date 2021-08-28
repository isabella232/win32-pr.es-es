---
description: Notifica a una aplicación cuando un IME está a punto de cerrar la ventana candidatos. La aplicación recibe este comando a través del mensaje WM \_ IME \_ NOTIFY con la configuración de parámetros, como se muestra a continuación.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: IMN_CLOSECANDIDATE de notificación (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd0a71eac28b2c7dc170724e40c9b4ba6707cd5774145f38efdd791e7ebd8b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107155"
---
# <a name="imn_closecandidate-notification-code"></a>Código de notificación \_ CLOSECANDIDATE de IMN

Notifica a una aplicación cuando un IME está a punto de cerrar la ventana candidatos. La aplicación recibe este comando a través del mensaje [**\_ WM IME \_ NOTIFY**](wm-ime-notify.md) con la configuración de parámetros, como se muestra a continuación.


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMN \_ CLOSECANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Marca de lista de candidatos. Cada bit corresponde a una lista de candidatos: bit 0 a la primera lista, bit 1 al segundo, y así sucesivamente. Si un bit especificado es 1, la ventana de candidatos correspondiente está a punto de cerrarse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este comando no tiene ningún valor devuelto.

## <a name="remarks"></a>Comentarios

Una aplicación debe procesar este comando si muestra los candidatos.

De forma predeterminada, la ventana IME destruye una ventana candidata cuando procesa este comando.

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

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




