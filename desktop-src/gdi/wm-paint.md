---
Description: El mensaje WM PAINT se envía cuando el sistema u otra aplicación realiza una solicitud \_ para pintar una parte de la ventana de una aplicación.
ms.assetid: afebaa07-cf00-47db-a919-46436f164881
title: WM_PAINT mensaje (Winuser.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: b5efec4bc92fcb3c90a8def59b2e85d98342cf641dfe959fc2a651f81ffc1f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092515"
---
# <a name="wm_paint-message"></a>Mensaje \_ DE WM PAINT

El **mensaje \_ WM PAINT** se envía cuando el sistema u otra aplicación realiza una solicitud para pintar una parte de la ventana de una aplicación. El mensaje se envía cuando se llama a la función [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) o [**RedrawWindow,**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) o bien mediante la función [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) cuando la aplicación obtiene un mensaje **WM \_ PAINT** mediante la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea)

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Ejemplo de [Windows ejemplos clásicos](https://github.com/microsoft/Windows-classic-samples/blob/18cbd05ee44455cd7552804dcf2c9d6db619b412/Samples/Win7Samples/begin/LearnWin32/HelloWorld/cpp/main.cpp) en GitHub.

## <a name="remarks"></a>Comentarios

El sistema genera el mensaje **WM \_ PAINT** y no lo debe enviar una aplicación. Para forzar que una ventana dibuje en un contexto de dispositivo específico, use el mensaje [**WM \_ PRINT**](wm-print.md) o [**WM \_ PRINTCLIENT.**](wm-printclient.md) Tenga en cuenta que esto requiere que la ventana de destino admita el **\_ mensaje PRINTCLIENT de WM.** Los controles más comunes admiten el **\_ mensaje PRINTCLIENT de WM.**

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  valida la región de actualización. La función también puede enviar el mensaje [**\_ WM NCPAINT**](wm-ncpaint.md) al procedimiento de ventana si se debe pintar el marco de ventana y enviar el mensaje [**\_ ERASEB DOMAINND**](../winmsg/wm-erasebkgnd.md) de WM si se debe borrar el fondo de la ventana.

El sistema envía este mensaje cuando no hay ningún otro mensaje en la cola de mensajes de la aplicación. [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) determina dónde enviar el mensaje; [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) determina qué mensaje se va a enviar. **GetMessage** devuelve el **mensaje WM \_ PAINT** cuando no hay ningún otro mensaje en la cola de mensajes de la aplicación y **DispatchMessage** envía el mensaje al procedimiento de ventana adecuado.

Una ventana puede recibir mensajes internos de pintura como resultado de llamar a [**RedrawWindow con**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) la marca INTERNALPAINT de RDW \_ establecida. En este caso, es posible que la ventana no tenga una región de actualización. Una aplicación puede llamar a [**la función GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) para determinar si la ventana tiene una región de actualización. Si **GetUpdateRect** devuelve cero, la aplicación no necesita llamar a las [**funciones BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) [**y EndPaint.**](/windows/desktop/api/Winuser/nf-winuser-endpaint)

Una aplicación debe comprobar si hay cuadros internos necesarios si observa sus estructuras de datos internas para cada mensaje **WM \_ PAINT,** ya que un mensaje WM PAINT puede deberse a una región de actualización que no es NULL y a una llamada a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con la marca INTERNALPAINT de **RDW \_** \_ establecida.

El sistema envía un mensaje **WM \_ PAINT** interno solo una vez. Después de que [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)devuelve un mensaje INTERNO de **WM \_ PAINT** desde [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o se envía a una ventana mediante UpdateWindow , el sistema no publica ni envía más mensajes **WM \_ PAINT** hasta que se invalida la ventana o hasta que se vuelve a llamar a [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con la marca INTERNALPAINT de RDW \_ establecida.

Para algunos controles comunes, el procesamiento de **mensajes \_ WM PAINT** predeterminado comprueba el parámetro *wParam.* Si *wParam no* es NULL, el control supone que el valor es un HDC y pinta con ese contexto de dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre dibujo y dibujo](painting-and-drawing.md)
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

[**Volver a dibujarWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> <dt>

[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)
</dt> <dt>

[**WM \_ ERASEBND**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ NCPAINT**](wm-ncpaint.md)
</dt> <dt>

[**WM \_ PRINT**](wm-print.md)
</dt> <dt>

[**WM \_ PRINTCLIENT**](wm-printclient.md)
</dt> </dl>

 

 
