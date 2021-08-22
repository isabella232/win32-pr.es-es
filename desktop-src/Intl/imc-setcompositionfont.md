---
description: Indica a una ventana de IME que especifique la fuente lógica que se usará para mostrar caracteres intermedios en la ventana de composición. Para enviar este comando, la aplicación usa el mensaje WM \_ IME \_ CONTROL con la configuración de parámetros que se muestra a continuación.
ms.assetid: 17b222e7-bf57-4cdd-8475-d9a8be03ab7f
title: IMC_SETCOMPOSITIONFONT comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ebc9f435371d4ae08b12191419c95fd53c69256064f0e90bb654e75fab922f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949276"
---
# <a name="imc_setcompositionfont-command"></a>Comando \_ SETCOMPOSITIONFONT de IMC

Indica a una ventana de IME que especifique la fuente lógica que se usará para mostrar caracteres intermedios en la ventana de composición. Para enviar este comando, la aplicación usa el mensaje [**WM \_ IME \_ CONTROL**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Establezca en IMC \_ SETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Puntero a una [**estructura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contiene información sobre la fuente lógica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente o un valor distinto de cero de lo contrario.

## <a name="remarks"></a>Comentarios

Al procesar este comando, la ventana IME cambia la fuente seleccionada actual en el contexto de entrada.

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

 

 
