---
description: Indica a una ventana de IME que establezca el estilo de la ventana de composición. Para enviar este comando, la aplicación usa el mensaje WM \_ IME \_ CONTROL con la configuración de parámetros que se muestra a continuación.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: IMC_SETCOMPOSITIONWINDOW comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb1fe35ecd530e8173b7ea57f7c6ff414105d09507a11bf4eed29ab0595e604
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107265"
---
# <a name="imc_setcompositionwindow-command"></a>Comando \_ SETCOMPOSITIONWINDOW de IMC

Indica a una ventana de IME que establezca el estilo de la ventana de composición. Para enviar este comando, la aplicación usa el mensaje [**WM \_ IME \_ CONTROL**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMC \_ SETCOMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntero a una [**estructura COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) que contiene la información de estilo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente o un valor distinto de cero de lo contrario.

## <a name="remarks"></a>Comentarios

Este comando establece el estilo en el contexto de entrada actual y el estilo se aplica posteriormente a cada ventana de IME que recibe ese contexto de entrada.

De forma predeterminada, la ventana IME tiene el estilo CFS \_ POINT. Con este estilo, la ventana de IME usa la posición de caret actual y el área de cliente de ventana cuando abre cualquier ventana de composición.

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
</dt> <dt>

[**WM \_ IME \_ CONTROL**](wm-ime-control.md)
</dt> </dl>

 

 




