---
description: Indica a la ventana IME que muestre la ventana de estado. Para enviar este comando, la aplicación usa el mensaje \_ WM IME \_ CONTROL con la configuración de parámetros que se muestra a continuación.
ms.assetid: 8c422592-ef59-4030-b684-81e4e552c6b0
title: IMC_OPENSTATUSWINDOW comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 263640a3f104c9abf72a7eb5b33bce6ff3813ca40645c18b179b9b31a95fdda9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107295"
---
# <a name="imc_openstatuswindow-command"></a>Comando \_ OPENSTATUSWINDOW de IMC

Indica a la ventana IME que muestre la ventana de estado. Para enviar este comando, la aplicación usa el mensaje [**\_ WM IME \_ CONTROL**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_OPENSTATUSWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMC \_ OPENSTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente o un valor distinto de cero en caso contrario.

## <a name="remarks"></a>Comentarios

Este comando se omite si el sistema operativo no está en el modo mostrar estado de IME. El usuario puede establecer o borrar el modo mostrar estado de IME desde la barra de tareas.

Si ya se muestra la ventana de estado, este comando no hace nada. Aunque la aplicación puede enviar este comando a la ventana de IME, la aplicación no recibe el comando [**\_ OPENSTATUSWINDOW de IMN**](imn-openstatuswindow.md) correspondiente.

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

[**WM \_ IME \_ CONTROL**](wm-ime-control.md)
</dt> </dl>

 

 




