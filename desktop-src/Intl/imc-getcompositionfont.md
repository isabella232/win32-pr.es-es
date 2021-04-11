---
description: Indica a una ventana de IME que recupere la fuente lógica usada para mostrar caracteres intermedios en la ventana de composición. Para enviar este comando, la aplicación usa el mensaje de control de IME de WM \_ \_ con la configuración de parámetros que se muestra a continuación.
ms.assetid: 43db70b6-f8bc-4241-9096-5d91fd1e332b
title: Comando IMC_GETCOMPOSITIONFONT (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 696d9809cadbe4f2c0e632719401e882777888dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275568"
---
# <a name="imc_getcompositionfont-command"></a>\_Comando IMC GETCOMPOSITIONFONT

Indica a una ventana de IME que recupere la fuente lógica usada para mostrar caracteres intermedios en la ventana de composición. Para enviar este comando, la aplicación usa el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) con la configuración de parámetros que se muestra a continuación.


```C++
LRESULT IMC_GETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Establezca en IMC \_ GETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Puntero a una estructura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que recibe información sobre la fuente lógica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se realiza correctamente, o un valor distinto de cero en caso contrario.

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
</dt> </dl>

 

 
