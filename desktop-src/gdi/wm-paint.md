---
Description: El mensaje de dibujo de WM \_ se envía cuando el sistema u otra aplicación realiza una solicitud para pintar una parte de la ventana de una aplicación.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: Mensaje de WM_PAINT (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b13e1779fb54a3db7905cb8fc738ef45558400f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987505"
---
# <a name="wm_paint-message"></a>Mensaje de Paint de WM \_

El mensaje de **\_ dibujo de WM** se envía cuando el sistema u otra aplicación realiza una solicitud para pintar una parte de la ventana de una aplicación. El mensaje se envía cuando se llama a la función [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) o [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) , o mediante la función [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) cuando la aplicación obtiene un mensaje de **\_ dibujo de WM** mediante la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación devuelve cero si procesa este mensaje.

## <a name="example"></a>Ejemplo

```c
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(hwnd, &ps);

            // All painting occurs here, between BeginPaint and EndPaint.
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(hwnd, &ps);
        }
        return 0;
    }

    return DefWindowProc(hwnd, uMsg, wParam, lParam);
}

```

Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) en github.

## <a name="remarks"></a>Observaciones

El sistema genera el mensaje de **\_ Paint de WM** y no debe ser enviado por una aplicación. Para forzar que una ventana dibuje en un contexto de dispositivo específico, use el mensaje [**WM \_ Print**](wm-print.md) o [**WM \_ PRINTCLIENT**](wm-printclient.md) . Tenga en cuenta que esto requiere que la ventana de destino admita el mensaje de **\_ PRINTCLIENT de WM** . Los controles más comunes admiten el mensaje de **\_ PRINTCLIENT de WM** .

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  valida la región de actualización. La función también puede enviar el mensaje de [**\_ NCPAINT de WM**](wm-ncpaint.md) al procedimiento de ventana si se debe pintar el marco de la ventana y enviar el mensaje de [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) si el fondo de la ventana debe borrarse.

El sistema envía este mensaje cuando no hay otros mensajes en la cola de mensajes de la aplicación. [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determina dónde se debe enviar el mensaje; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determina el mensaje que se va a enviar. **GetMessage** devuelve el mensaje de **\_ dibujo de WM** cuando no hay ningún otro mensaje en la cola de mensajes de la aplicación y **DispatchMessage** envía el mensaje al procedimiento de ventana adecuado.

Una ventana puede recibir mensajes de dibujo internos como resultado de llamar a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con el \_ conjunto de marcas RDW INTERNALPAINT. En este caso, es posible que la ventana no tenga una región de actualización. Una aplicación puede llamar a la función [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) para determinar si la ventana tiene una región de actualización. Si **GetUpdateRect** devuelve cero, la aplicación no necesita llamar a las funciones [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) y [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) .

Una aplicación debe comprobar los dibujos internos necesarios examinando sus estructuras de datos internas para cada mensaje **de \_ pintura de WM** , ya que es posible que un mensaje de **\_ Paint de WM** esté causado por una región de actualización que no sea NULL y una llamada a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con el \_ indicador RDW INTERNALPAINT establecido.

El sistema envía un mensaje **de \_ dibujo de WM** interno solo una vez. Una vez que se devuelve un mensaje de **\_ dibujo de WM** interno desde [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o se envía a una ventana por [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow), el sistema no expone ni envía más mensajes de la **\_ pintura de WM** hasta que no se invalida la ventana o hasta que se llama de nuevo a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con la \_ marca RDW INTERNALPAINT establecida.

Para algunos controles comunes, el procesamiento de mensajes de **\_ pintura de WM** predeterminado comprueba el parámetro *wParam* . Si *wParam* no es null, el control supone que el valor es HDC y pinta usando ese contexto de dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre pintura y dibujo](painting-and-drawing.md)
</dt> <dt>

[Pintar y dibujar mensajes](painting-and-drawing-messages.md)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**ERASEBKGND de WM \_**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**NCPAINT de WM \_**](wm-ncpaint.md)
</dt> <dt>

[**impresión de WM \_**](wm-print.md)
</dt> <dt>

[**PRINTCLIENT de WM \_**](wm-printclient.md)
</dt> </dl>

 

 
