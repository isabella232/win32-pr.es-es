---
description: Indica a una ventana del IME que establezca el estilo de la ventana de composición. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: 19b99228-a1fc-4cd5-8f37-5462bf767f85
title: Comando IMC_SETCOMPOSITIONWINDOW (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b06c53b1ff2ec343d6382dd48d0d4108cf403c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686922"
---
# <a name="imc_setcompositionwindow-command"></a>\_Comando IMC SETCOMPOSITIONWINDOW

Indica a una ventana del IME que establezca el estilo de la ventana de composición. Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMC \_ SETCOMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a una estructura [**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform) que contiene la información de estilo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.

## <a name="remarks"></a>Observaciones

Este comando establece el estilo en el contexto de entrada actual y el estilo se aplica posteriormente a cada ventana del IME que recibe ese contexto de entrada.

De forma predeterminada, la ventana del IME tiene el estilo de punto de CFS \_ . Con este estilo, la ventana del IME usa la posición del símbolo de intercalación actual y el área de cliente de la ventana cuando abre cualquier ventana de composición.

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

[**COMPOSITIONFORM**](/windows/win32/api/imm/ns-imm-compositionform)
</dt> <dt>

[**\_control IME de WM \_**](wm-ime-control.md)
</dt> </dl>

 

 




