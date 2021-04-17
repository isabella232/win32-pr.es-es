---
description: Se envía cuando se debe calcular el tamaño y la posición del área de cliente de una ventana. Al procesar este mensaje, una aplicación puede controlar el contenido del área de cliente de la ventana cuando cambia el tamaño o la posición de la ventana.
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: Mensaje de WM_NCCALCSIZE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7d63fea3ad0a80bba686d8d86aa5354f0bb45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716044"
---
# <a name="wm_nccalcsize-message"></a>Mensaje de NCCALCSIZE de WM \_

Se envía cuando se debe calcular el tamaño y la posición del área de cliente de una ventana. Al procesar este mensaje, una aplicación puede controlar el contenido del área de cliente de la ventana cuando cambia el tamaño o la posición de la ventana.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Si *wParam* es **true**, especifica que la aplicación debe indicar qué parte del área de cliente contiene información válida. El sistema copia la información válida en el área especificada dentro del nuevo área cliente.

Si *wParam* es **false**, no es necesario que la aplicación indique la parte válida del área cliente.

</dd> <dt>

*lParam* 
</dt> <dd>

Si *wParam* es **true**, *lParam* apunta a una [**estructura \_ params NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) que contiene información que una aplicación puede utilizar para calcular el nuevo tamaño y la posición del rectángulo del cliente.

Si *wParam* es **false**, *lParam* apunta a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) . En la entrada, la estructura contiene el rectángulo de ventana propuesto para la ventana. Al salir, la estructura debe contener las coordenadas de pantalla del área cliente de la ventana correspondiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si el parámetro *wParam* es **false**, la aplicación debe devolver cero.

Si *wParam* es **true**, la aplicación debe devolver cero o una combinación de los valores siguientes.

Si *wParam* es **true** y una aplicación devuelve cero, el área cliente anterior se conserva y se alinea con la esquina superior izquierda del área cliente nueva.



| Código o valor devuelto                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**WVR \_ ALIGNTOP**</dt> <dt>0x0010</dt> </dl>    | Especifica que el área cliente de la ventana se va a conservar y alinear con la parte superior de la nueva posición de la ventana. Por ejemplo, para alinear el área de cliente en la esquina superior izquierda, devuelva los valores de WVR \_ ALIGNTOP y **WVR \_ ALIGNLEFT** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**WVR \_ ALIGNRIGHT**</dt> <dt>0x0080</dt> </dl>  | Especifica que el área cliente de la ventana se va a conservar y alinear con el lado derecho de la nueva posición de la ventana. Por ejemplo, para alinear el área cliente a la esquina inferior derecha, devuelva los valores de **WVR \_ ALIGNRIGHT** y WVR \_ ALIGNBOTTOM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**WVR \_ ALIGNLEFT**</dt> <dt>0x0020</dt> </dl>   | Especifica que el área cliente de la ventana se va a conservar y alinear con el lado izquierdo de la nueva posición de la ventana. Por ejemplo, para alinear el área cliente en la esquina inferior izquierda, devuelva los valores de **WVR \_ ALIGNLEFT** y **WVR \_ ALIGNBOTTOM** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**WVR \_ ALIGNBOTTOM**</dt> <dt>0x0040</dt> </dl> | Especifica que el área cliente de la ventana se va a conservar y alinear con la parte inferior de la nueva posición de la ventana. Por ejemplo, para alinear el área de cliente con la esquina superior izquierda, devuelva los valores de WVR \_ ALIGNTOP y **WVR \_ ALIGNLEFT** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**WVR \_ HREDRAW**</dt> <dt>0x0100</dt> </dl>     | Se usa en combinación con cualquier otro valor, excepto **WVR \_ VALIDRECTS**, hace que la ventana se vuelva a dibujar completamente si el rectángulo del cliente cambia el tamaño horizontalmente. Este valor es similar al estilo de clase [CS \_ HREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**WVR \_ VREDRAW**</dt> <dt>0x0200</dt> </dl>     | Se usa en combinación con cualquier otro valor, excepto **WVR \_ VALIDRECTS**, hace que la ventana se vuelva a dibujar completamente si el rectángulo del cliente cambia el tamaño verticalmente. Este valor es similar al estilo de clase [CS \_ VREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**WVR \_ Volver a dibujar**</dt> <dt>0x0300</dt> </dl>      | Este valor hace que se vuelva a dibujar toda la ventana. Es una combinación de valores de **WVR \_ HREDRAW** y **WVR \_ VREDRAW** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**WVR \_ VALIDRECTS**</dt> <dt>0x0400</dt> </dl>  | Este valor indica que, cuando se devuelve de [**WM \_ NCCALCSIZE**](wm-nccalcsize.md), los rectángulos especificados por los miembros **rgrc** \[ 1 \] y **rgrc** \[ 2 \] de la estructura [**\_ params NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) contienen rectángulos de área de origen y de destino válidos, respectivamente. El sistema combina estos rectángulos para calcular el área de la ventana que se va a conservar. El sistema copia cualquier parte de la imagen de la ventana que se encuentra dentro del rectángulo de origen y recorta la imagen al rectángulo de destino. Ambos rectángulos están en coordenadas relativas al primario o a la pantalla. Esta marca no se puede combinar con ningún otro marcador. <br/> Este valor devuelto permite a una aplicación implementar estrategias de preservación del área cliente más elaboradas, como centrar o conservar un subconjunto del área cliente.<br/> |



 

## <a name="remarks"></a>Observaciones

La ventana puede volver a dibujarse, dependiendo de si se ha especificado el estilo de clase [CS \_ HREDRAW](about-window-classes.md) o CS \_ VREDRAW. Este es el procesamiento predeterminado compatible con versiones anteriores de este mensaje mediante la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) (además del cálculo de rectángulo de cliente habitual descrito en la tabla anterior).

Cuando *wParam* es **true**, simplemente si se devuelve 0 sin procesar los rectángulos de los [**\_ parámetros de NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) , el área cliente cambiará de tamaño al tamaño de la ventana, incluido el marco de la ventana. Esto quitará el marco de ventana y los elementos de título de la ventana, pero solo se mostrará el área cliente.

A partir de Windows Vista, quitar el fotograma estándar simplemente devolviendo 0 cuando el **valor** de *wParam* es true no afecta a los fotogramas que se extienden en el área de cliente mediante la función [**DwmExtendFrameIntoClientArea**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) . Solo se quitará el fotograma estándar.

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

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**PARÁMETROS de NCCALCSIZE \_**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
