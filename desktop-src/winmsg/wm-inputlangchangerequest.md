---
description: Se publica en la ventana con el foco cuando el usuario elige un nuevo idioma de entrada, ya sea con la tecla de acceso rápido (especificada en la aplicación del panel de control Teclado) o desde el indicador de la barra de tareas del sistema.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: WM_INPUTLANGCHANGEREQUEST mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644fa4764c5172edc34f16509c6a6b00be6356b80c460a08233be8aa64ef69c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056065"
---
# <a name="wm_inputlangchangerequest-message"></a>Mensaje \_ INPUTLANGCHANGEREQUEST de WM

Se publica en la ventana con el foco cuando el usuario elige un nuevo idioma de entrada, ya sea con la tecla de acceso rápido (especificada en la aplicación del panel de control Teclado) o desde el indicador de la barra de tareas del sistema. Una aplicación puede aceptar el cambio pasando el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o rechazar el cambio (e impedir que se haga) devolviendo inmediatamente.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nueva configuración regional de entrada. Este parámetro puede ser una combinación de las marcas siguientes.



| Value                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <dt>**INPUTLANGCHANGE \_ Backward**</dt> <dt>0x0004</dt> </dl>       | Se usó una tecla de acceso para elegir la configuración regional de entrada anterior en la lista instalada de configuraciones regionales de entrada. Esta marca no se puede usar con la marca INPUTLANGCHANGE \_ FORWARD.<br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <dt>**INPUTLANGCHANGE \_ Reenvío**</dt> <dt>0x0002</dt> </dl>          | Se usó una tecla de acceso derecho para elegir la siguiente configuración regional de entrada en la lista instalada de configuraciones regionales de entrada. Esta marca no se puede usar con la marca INPUTLANGCHANGE \_ BACKWARD.<br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <dt>**INPUTLANGCHANGE \_ SysCHARSET**</dt> <dt>0x0001</dt> </dl> | El diseño del teclado de la nueva configuración regional de entrada se puede usar con el juego de caracteres del sistema.<br/>                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de configuración regional de entrada. Para obtener más información, [vea Idiomas, configuraciones regionales y diseños de teclado.](../inputdev/about-keyboard-input.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Este mensaje se publica, no se envía, a la aplicación, por lo que se omite el valor devuelto. Para aceptar el cambio, la aplicación debe pasar el mensaje [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Para rechazar el cambio, la aplicación debe devolver cero sin llamar **a DefWindowProc**.

## <a name="remarks"></a>Comentarios

Cuando la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) recibe el mensaje **\_ INPUTLANGCHANGEREQUEST** de WM, activa la nueva configuración regional de entrada y notifica a la aplicación el cambio mediante el envío del [**mensaje \_ INPUTLANGCHANGE de WM.**](wm-inputlangchange.md)

El indicador de idioma solo está presente en la barra de tareas si ha instalado más de un diseño de teclado y si ha habilitado el indicador mediante la aplicación del panel de control Teclado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
