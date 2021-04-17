---
description: Se envía a la ventana con el foco cuando el usuario elige un nuevo idioma de entrada, ya sea con la tecla de rápida (especificada en la aplicación del panel de control del teclado) o desde el indicador en la barra de tareas del sistema.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: Mensaje de WM_INPUTLANGCHANGEREQUEST (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697164"
---
# <a name="wm_inputlangchangerequest-message"></a>Mensaje de INPUTLANGCHANGEREQUEST de WM \_

Se envía a la ventana con el foco cuando el usuario elige un nuevo idioma de entrada, ya sea con la tecla de rápida (especificada en la aplicación del panel de control del teclado) o desde el indicador en la barra de tareas del sistema. Una aplicación puede aceptar el cambio pasando el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o rechazar el cambio (e impedir que tenga lugar) devolviendo inmediatamente.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La nueva configuración regional de entrada. Este parámetro puede ser una combinación de las marcas siguientes.



| Value                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0004</dt> atrás </dl>       | Se usó una tecla de acceso rápido para elegir la configuración regional de entrada anterior en la lista instalada de configuraciones regionales de entrada. Esta marca no se puede usar con la \_ marca de avance de INPUTLANGCHANGE.<br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <dt>**INPUTLANGCHANGE \_ Reenvío**</dt> de <dt>0x0002</dt> </dl>          | Se usó una tecla de acceso rápido para elegir la configuración regional de entrada siguiente en la lista instalada de configuraciones regionales de entrada. Esta marca no se puede usar con la \_ marca atrás de INPUTLANGCHANGE.<br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <dt>**INPUTLANGCHANGE \_ SYSCHARSET**</dt> <dt>0x0001</dt> </dl> | La nueva distribución del teclado de la configuración regional de entrada se puede usar con el juego de caracteres del sistema.<br/>                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de configuración regional de entrada. Para obtener más información, consulte [idiomas, configuraciones regionales y distribuciones del teclado](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Este mensaje se publica, no se envía a la aplicación, por lo que se omite el valor devuelto. Para aceptar el cambio, la aplicación debe pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Para rechazar el cambio, la aplicación debe devolver cero sin llamar a **DefWindowProc**.

## <a name="remarks"></a>Observaciones

Cuando la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) recibe el mensaje de **\_ INPUTLANGCHANGEREQUEST de WM** , activa la nueva configuración regional de entrada y notifica a la aplicación el cambio mediante el envío del mensaje de [**\_ INPUTLANGCHANGE de WM**](wm-inputlangchange.md) .

El indicador de idioma solo está presente en la barra de tareas si se ha instalado más de una distribución de teclado y se ha habilitado el indicador mediante la aplicación del panel de control del teclado.

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

[**INPUTLANGCHANGE de WM \_**](wm-inputlangchange.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
