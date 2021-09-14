---
description: Indica a la ventana IME que oculte la ventana de estado. Para enviar este comando, la aplicación usa el mensaje WM \_ IME \_ CONTROL con la configuración de parámetros que se muestra a continuación.
ms.assetid: e3da5962-a652-409e-b0ec-eb93671049b4
title: IMC_CLOSESTATUSWINDOW comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 207f04d53f269318f87ed11038cbd6817d5e607e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063133"
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

## <a name="remarks"></a>Observaciones

Cuando la ventana de estado de IME ya está oculta, este comando no hace nada. Aunque una aplicación puede enviar este comando a la ventana de IME, la aplicación no recibe el comando [ \_ CLOSESTATUSWINDOW de IMN](imn-closestatuswindow.md) correspondiente.

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
</dt> </dl>

 

 




