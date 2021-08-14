---
description: Se envía cuando se debe calcular el tamaño y la posición del área cliente de una ventana. Al procesar este mensaje, una aplicación puede controlar el contenido del área cliente de la ventana cuando cambia el tamaño o la posición de la ventana.
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: WM_NCCALCSIZE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f0a73b469a920bcba79cc19670a7b9536c1bac9e0b0ffcab7ddf5930b984dae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200081"
---
# <a name="wm_nccalcsize-message"></a>Mensaje \_ WM NCCALCSIZE

Se envía cuando se debe calcular el tamaño y la posición del área cliente de una ventana. Al procesar este mensaje, una aplicación puede controlar el contenido del área cliente de la ventana cuando cambia el tamaño o la posición de la ventana.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Si *wParam es* **TRUE,** especifica que la aplicación debe indicar qué parte del área de cliente contiene información válida. El sistema copia la información válida en el área especificada dentro del nuevo área de cliente.

Si *wParam* es **FALSE,** la aplicación no necesita indicar la parte válida del área de cliente.

</dd> <dt>

*lParam* 
</dt> <dd>

Si *wParam* es **TRUE,** *lParam* apunta a una estructura [**NCCALCSIZE \_ PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) que contiene información que una aplicación puede usar para calcular el nuevo tamaño y la posición del rectángulo del cliente.

Si *wParam es* **FALSE,** *lParam* apunta a una [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) En la entrada, la estructura contiene el rectángulo de ventana propuesto para la ventana. Al salir, la estructura debe contener las coordenadas de pantalla del área cliente de ventana correspondiente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si el *parámetro wParam* es **FALSE,** la aplicación debe devolver cero.

Si *wParam es* **TRUE,** la aplicación debe devolver cero o una combinación de los valores siguientes.

Si *wParam* es **TRUE** y una aplicación devuelve cero, el área de cliente antigua se conserva y se alinea con la esquina superior izquierda del nuevo área de cliente.



| Código o valor devuelto                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**WVR \_ AlignTOP**</dt> <dt>0x0010</dt> </dl>    | Especifica que el área cliente de la ventana se va a conservar y alinear con la parte superior de la nueva posición de la ventana. Por ejemplo, para alinear el área de cliente con la esquina superior izquierda, devuelva los valores de WVR ALIGNTOP y \_ **WVR \_ ALIGNLEFT.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**WVR \_ ALIGNRIGHT**</dt> <dt>0x0080</dt> </dl>  | Especifica que el área cliente de la ventana se va a conservar y alinear con el lado derecho de la nueva posición de la ventana. Por ejemplo, para alinear el área de cliente con la esquina inferior derecha, devuelva los valores **de WVR \_ ALIGNRIGHT** y WVR \_ ALIGNBOTTOM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**WVR \_ AlignLEFT**</dt> <dt>0x0020</dt> </dl>   | Especifica que el área cliente de la ventana se va a conservar y alinear con el lado izquierdo de la nueva posición de la ventana. Por ejemplo, para alinear el área de cliente con la esquina inferior izquierda, devuelva los valores **de WVR \_ ALIGNLEFT** y **WVR \_ ALIGNBOTTOM.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**WVR \_ AlignBOTTOM**</dt> <dt>0x0040</dt> </dl> | Especifica que el área cliente de la ventana se va a conservar y alinear con la parte inferior de la nueva posición de la ventana. Por ejemplo, para alinear el área de cliente con la esquina superior izquierda, devuelva los valores de WVR ALIGNTOP y \_ **WVR \_ ALIGNLEFT.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**WVR \_ HREDRAW**</dt> <dt>0x0100</dt> </dl>     | Se usa en combinación con cualquier otro valor, excepto **WVR \_ VALIDRECTS,** lo que hace que la ventana se vuelva a dibujar completamente si el rectángulo del cliente cambia de tamaño horizontalmente. Este valor es similar al estilo [de clase \_ HREDRAW de CS](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**WVR \_ DRAWDRAW**</dt> <dt>0x0200</dt> </dl>     | Se usa en combinación con cualquier otro valor, excepto **WVR \_ VALIDRECTS,** lo que hace que la ventana se vuelva a dibujar completamente si el rectángulo del cliente cambia de tamaño verticalmente. Este valor es similar al [estilo de clase \_ DRAWDRAW](about-window-classes.md) de CS<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**WVR \_ Volver a dibujar**</dt> <dt>0x0300</dt> </dl>      | Este valor hace que se vuelva a dibujar toda la ventana. Es una combinación de los **valores de WVR \_ HREDRAW** y **WVR \_ DRAW.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**WVR \_ ValidRECTS**</dt> <dt>0x0400</dt> </dl>  | Este valor indica que, tras la devolución de [**WM \_ NCCALCSIZE,**](wm-nccalcsize.md)los rectángulos especificados por los miembros **rgrc** 1 y rgrc 2 de la estructura NCCALCSIZE PARAMS contienen rectángulos de destino y área de origen \[ \]  \[ \] válidos, respectivamente. [**\_**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) El sistema combina estos rectángulos para calcular el área de la ventana que se va a conservar. El sistema copia cualquier parte de la imagen de ventana que se encuentra dentro del rectángulo de origen y recorta la imagen al rectángulo de destino. Ambos rectángulos están en coordenadas relativas a elementos primarios o relativos a la pantalla. Esta marca no se puede combinar con ninguna otra marca. <br/> Este valor devuelto permite a una aplicación implementar estrategias de conservación del área de cliente más elaborados, como centrar o conservar un subconjunto del área cliente.<br/> |



 

## <a name="remarks"></a>Comentarios

La ventana se puede volver a dibujar, dependiendo de si se especifica el estilo de clase [ \_ CS HREDRAW](about-window-classes.md) o CS \_ DRAWDRAW. Este es el procesamiento predeterminado compatible con versiones anteriores de este mensaje por parte de la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) (además del cálculo habitual del rectángulo de cliente descrito en la tabla anterior).

Cuando *wParam* es **TRUE,** devolver simplemente 0 sin procesar los rectángulos [**NCCALCSIZE \_ PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) hará que el área de cliente cambie de tamaño al tamaño de la ventana, incluido el marco de ventana. Esto quitará el marco de ventana y los elementos de título de la ventana, dejando solo el área de cliente mostrada.

A partir de Windows Vista, quitar el marco estándar simplemente devolviendo 0 cuando *wParam* es **TRUE** no afecta a los fotogramas que se extienden al área cliente mediante la función [**DwmExtendFrameIntoClientArea.**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) Solo se quitará el marco estándar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**NCCALCSIZE \_ PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
