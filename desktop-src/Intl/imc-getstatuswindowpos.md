---
description: Indica a una ventana de IME que obtenga la posición de la ventana de estado. Para enviar este comando, la aplicación usa el mensaje \_ WM IME \_ CONTROL con la configuración de parámetros que se muestra a continuación.
ms.assetid: 59c7baae-1b8a-4761-9814-31afd8d39691
title: IMC_GETSTATUSWINDOWPOS comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd17c5787d9ef8c787e62a556afa2f136bd65c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063130"
---
# <a name="imc_getstatuswindowpos-command"></a>Comando \_ GETSTATUSWINDOWPOS de IMC

Indica a una ventana de IME que obtenga la posición de la ventana de estado. Para enviar este comando, la aplicación usa el mensaje [**\_ WM IME \_ CONTROL**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_GETSTATUSWINDOWPOS
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMC \_ GETSTATUSWINDOWPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una [**estructura POINTS que**](/previous-versions//dd162808(v=vs.85)) contiene la coordenada x y la coordenada y de la posición de la ventana de estado en coordenadas de pantalla, en relación con la esquina superior izquierda de la pantalla.

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

[**WM \_ IME \_ CONTROL**](wm-ime-control.md)
</dt> </dl>

 

 
