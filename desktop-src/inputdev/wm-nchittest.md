---
title: Mensaje de WM_NCHITTEST (Winuser. h)
description: Se envía a una ventana para determinar qué parte de la ventana corresponde a una coordenada de pantalla determinada.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- Entrada de mouse y teclado de mensaje de WM_NCHITTEST
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695898"
---
# <a name="wm_nchittest-message"></a>Mensaje de NCHITTEST de WM \_

Se envía a una ventana para determinar qué parte de la ventana corresponde a una coordenada de pantalla determinada. Esto puede ocurrir, por ejemplo, cuando se mueve el cursor, cuando se presiona o se suelta un botón del mouse o en respuesta a una llamada a una función como [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint). Si no se captura el mouse, el mensaje se envía a la ventana debajo del cursor. De lo contrario, el mensaje se envía a la ventana que ha capturado el mouse.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica la coordenada x del cursor. La coordenada es relativa a la esquina superior izquierda de la pantalla.

La palabra de orden superior especifica la coordenada y del cursor. La coordenada es relativa a la esquina superior izquierda de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto de la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) es uno de los siguientes valores, que indica la posición de la zona activa del cursor.



| Código o valor devuelto                                                                                                                                    | Descripción                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**HTBORDER**</dt> <dt>18</dt> </dl>      | En el borde de una ventana que no tiene un borde de ajuste de tamaño.<br/>                                                                                                                                           |
| <dl> <dt>**HTBOTTOM**</dt> <dt>15</dt> </dl>      | En el borde inferior horizontal de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana verticalmente).<br/>                                                                                    |
| <dl> <dt>**HTBOTTOMLEFT**</dt> <dt>16</dt> </dl>  | En la esquina inferior izquierda de un borde de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana en diagonal).<br/>                                                                              |
| <dl> <dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt> </dl> | En la esquina inferior derecha de un borde de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana en diagonal).<br/>                                                                             |
| <dl> <dt>**HTCAPTION**</dt> <dt>2</dt> </dl>      | En una barra de título.<br/>                                                                                                                                                                                         |
| <dl> <dt>**HTCLIENT**</dt> <dt>1</dt> </dl>       | En un área cliente.<br/>                                                                                                                                                                                       |
| <dl> <dt>**HTCLOSE**</dt> <dt>20</dt> </dl>       | En un botón **cerrar** .<br/>                                                                                                                                                                                  |
| <dl> <dt>**HTERROR**</dt> <dt>-2</dt> </dl>       | En el fondo de la pantalla o en una línea divisoria entre ventanas (igual que **HTNOWHERE**, con la excepción de que la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera un bip del sistema para indicar un error).<br/> |
| <dl> <dt>**HTGROWBOX**</dt> <dt>4</dt> </dl>      | En un cuadro de tamaño (igual que **HTSIZE**).<br/>                                                                                                                                                                     |
| <dl> <dt>**HTHELP**</dt> <dt>21</dt> </dl>        | En un botón **ayuda** .<br/>                                                                                                                                                                                   |
| <dl> <dt>**HTHSCROLL**</dt> <dt>6</dt> </dl>      | En una barra de desplazamiento horizontal.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTLEFT**</dt> <dt>10</dt> </dl>        | En el borde izquierdo de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana horizontalmente).<br/>                                                                                              |
| <dl> <dt>**HTMENU**</dt> <dt>5</dt> </dl>         | En un menú.<br/>                                                                                                                                                                                              |
| <dl> <dt>**HTMAXBUTTON**</dt> <dt>9</dt> </dl>    | En un botón **maximizar** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTMINBUTTON**</dt> <dt>8</dt> </dl>    | En un botón **minimizar** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTNOWHERE**</dt> <dt>0</dt> </dl>      | En el fondo de la pantalla o en una línea divisoria entre ventanas.<br/>                                                                                                                                         |
| <dl> <dt>**HTREDUCE**</dt> <dt>8</dt> </dl>       | En un botón **minimizar** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTRIGHT**</dt> <dt>11</dt> </dl>       | En el borde derecho de una ventana de tamaño variable (el usuario puede hacer clic con el mouse para cambiar el tamaño de la ventana horizontalmente).<br/>                                                                                             |
| <dl> <dt>**HTSIZE**</dt> <dt>4</dt> </dl>         | En un cuadro de tamaño (igual que **HTGROWBOX**).<br/>                                                                                                                                                                  |
| <dl> <dt>**HTSYSMENU**</dt> <dt>3</dt> </dl>      | En un menú ventana o en un botón **cerrar** de una ventana secundaria.<br/>                                                                                                                                            |
| <dl> <dt>**HTTOP**</dt> <dt>12</dt> </dl>         | En el borde superior horizontal de una ventana.<br/>                                                                                                                                                             |
| <dl> <dt>**HTTOPLEFT**</dt> <dt>13</dt> </dl>     | En la esquina superior izquierda de un borde de ventana.<br/>                                                                                                                                                            |
| <dl> <dt>**HTTOPRIGHT**</dt> <dt>14</dt> </dl>    | En la esquina superior derecha de un borde de ventana.<br/>                                                                                                                                                           |
| <dl> <dt>**HTTRANSPARENT**</dt> <dt>-1</dt> </dl> | En una ventana actualmente incluida en otra ventana del mismo subproceso (el mensaje se enviará a las ventanas subyacentes en el mismo subproceso hasta que uno de ellos devuelva un código que no sea **HTTRANSPARENT**).<br/>  |
| <dl> <dt>**HTVSCROLL**</dt> <dt>7</dt> </dl>      | En la barra de desplazamiento vertical.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTZOOM**</dt> <dt>9</dt> </dl>         | En un botón **maximizar** .<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

Use el código siguiente para obtener la posición horizontal y vertical:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Como se indicó anteriormente, la coordenada x está en el **corto** orden inferior del valor devuelto. la coordenada y está en el valor **Short** de orden superior (ambos representan valores *firmados* porque pueden tomar valores negativos en sistemas con varios monitores). Si el valor devuelto se asigna a una variable, puede usar la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) para obtener una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) del valor devuelto. También puede usar la macro [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) u [**Get \_ Y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para extraer la coordenada x o y.

> [!IMPORTANT]
> No use las macros [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) para extraer las coordenadas x e y de la posición del cursor porque estas macros devuelven resultados incorrectos en sistemas con varios monitores. Los sistemas con varios monitores pueden tener coordenadas x e y negativas, y **LOWORD** y **HIWORD** tratan las coordenadas como cantidades sin signo.

 

**Windows Vista:** Al crear fotogramas personalizados que incluyen los botones de título estándar, este mensaje debe pasarse primero a la función [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) . Esto permite que el Administrador de ventanas de escritorio (DWM) proporcione pruebas de posicionamiento para los botones de subtítulos. Si **DwmDefWindowProc** no controla el mensaje, es posible que se necesite un procesamiento adicional de **\_ NCHITTEST de WM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir windowsx. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OBTENER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTENER \_ \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada del mouse](mouse-input.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**CIMA**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

