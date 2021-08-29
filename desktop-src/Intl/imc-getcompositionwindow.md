---
description: Indica a una ventana de IME que obtenga la posición de la ventana de composición. Para enviar este comando, la aplicación usa el mensaje \_ WM IME \_ CONTROL con la configuración de parámetros que se muestra a continuación.
ms.assetid: d2c60974-a602-4a42-8a45-870ee39df001
title: IMC_GETCOMPOSITIONWINDOW comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc32c183377967071b5f0cdea278a37a414a7eead422a5ed00750174a6667bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068095"
---
# <a name="imc_getcompositionwindow-command"></a>Comando \_ GETCOMPOSITIONWINDOW de IMC

Indica a una ventana de IME que obtenga la posición de la ventana de composición. Para enviar este comando, la aplicación usa el mensaje [**\_ WM IME \_ CONTROL**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_GETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMC \_ GETCOMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntero a una [**estructura COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) que contiene la posición de la ventana de composición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente o un valor distinto de cero en caso contrario.

## <a name="remarks"></a>Comentarios

Dado que el IME podría ajustar la posición de una ventana de composición, una aplicación usa este comando para obtener la posición real para decidir si se va a cambiar la posición de la ventana. La posición recuperada se encuentra en coordenadas de ventana relativas a la ventana que tiene el foco de entrada actual.

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

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> </dl>

 

 




