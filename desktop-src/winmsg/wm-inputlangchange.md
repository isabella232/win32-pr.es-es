---
description: Se envía a la ventana de nivel superior afectada después de cambiar el idioma de entrada de una aplicación. Debe establecer cualquier configuración específica de la aplicación y pasar el mensaje a la función DefWindowProc, que pasa el mensaje a todas las ventanas secundarias de primer nivel.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Mensaje de WM_INPUTLANGCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154168"
---
# <a name="wm_inputlangchange-message"></a>Mensaje de INPUTLANGCHANGE de WM \_

Se envía a la ventana de nivel superior afectada después de cambiar el idioma de entrada de una aplicación. Debe establecer cualquier configuración específica de la aplicación y pasar el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , que pasa el mensaje a todas las ventanas secundarias de primer nivel. Estas ventanas secundarias pueden pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que pase el mensaje a sus ventanas secundarias, etc.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Juego de caracteres de la nueva configuración regional.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de configuración regional de entrada. Para obtener más información, consulte [idiomas, configuraciones regionales y distribuciones del teclado](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver un valor distinto de cero si procesa este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**INPUTLANGCHANGEREQUEST de WM \_**](wm-inputlangchangerequest.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
