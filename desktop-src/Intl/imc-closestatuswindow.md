---
description: Indica a la ventana IME que oculte la ventana de estado. Para enviar este comando, la aplicación usa el mensaje WM \_ IME \_ CONTROL con la configuración de parámetros que se muestra a continuación.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: IMC_CLOSESTATUSWINDOW comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31393c57c01f8f90d042e9bde1fe5bc742d606e099064e13f8de5baefeb46f58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107395"
---
# <a name="imc_closestatuswindow-command"></a>Comando \_ CLOSESTATUSWINDOW de IMC

Indica a la ventana IME que oculte la ventana de estado. Para enviar este comando, la aplicación usa el mensaje [**WM \_ IME \_ CONTROL**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_CLOSESTATUSWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMC \_ CLOSESTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente o un valor distinto de cero de lo contrario.

## <a name="remarks"></a>Comentarios

Cuando la ventana de estado de IME ya está oculta, este comando no hace nada. Aunque una aplicación puede enviar este comando a la ventana de IME, la aplicación no recibe el comando [ \_ CLOSESTATUSWINDOW de IMN](imn-closestatuswindow.md) correspondiente.

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
</dt> </dl>

 

 




