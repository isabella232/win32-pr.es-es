---
title: Dibujo con Direct2D
description: Después de crear los recursos de gráficos, está listo para dibujar.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487611"
---
# <a name="drawing-with-direct2d"></a>Dibujo con Direct2D

Después de crear los recursos de gráficos, está listo para dibujar.

## <a name="drawing-an-ellipse"></a>Dibujar una elipse

El programa de [círculo](your-first-direct2d-program.md) realiza una lógica de dibujo muy sencilla:

1.  Rellene el fondo con un color sólido.
2.  Dibuja un círculo relleno.

![captura de pantalla del programa de círculo.](images/graphics08.png)

Dado que el destino de representación es una ventana (en lugar de un mapa de bits u otra superficie fuera de la pantalla), el dibujo se realiza en respuesta a los mensajes de [**\_ pintura de WM**](/windows/desktop/gdi/wm-paint) . En el código siguiente se muestra el procedimiento de ventana para el programa de círculo.


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

Este es el código que dibuja el círculo.

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



La interfaz [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) se usa para todas las operaciones de dibujo. El método del programa `OnPaint` hace lo siguiente:

1.  El método [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) señala el inicio del dibujo.
2.  El método [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) llena todo el destino de representación con un color sólido. El color se proporciona como una [**estructura \_ \_ F de color D2D1**](/windows/desktop/Direct2D/d2d1-color-f) . Puede usar la clase [**D2D1:: ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) para inicializar la estructura. Para obtener más información, vea [usar el color en Direct2D](using-color-in-direct2d.md).
3.  El método [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dibuja una elipse rellena, utilizando el pincel especificado para el relleno. Una elipse se especifica mediante un punto central y los radios x e y. Si los radios x e y son iguales, el resultado es un círculo.
4.  El método [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) indica la finalización del dibujo para este marco. Todas las operaciones de dibujo se deben colocar entre las llamadas a [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) y **EndDraw**.

Todos los métodos [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)y [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) tienen un tipo de valor devuelto **void** . Si se produce un error durante la ejecución de cualquiera de estos métodos, el error se señaliza a través del valor devuelto del método [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . El `CreateGraphicsResources` método se muestra en el tema [crear recursos de Direct2D](render-targets--devices--and-resources.md). Este método crea el destino de representación y el pincel de color sólido.

El dispositivo puede almacenar en búfer los comandos de dibujo y aplazar su ejecución hasta que se llame a [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Puede forzar que el dispositivo ejecute cualquier comando de dibujo pendiente mediante una llamada a [**ID2D1RenderTarget:: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush). Sin embargo, el vaciado puede reducir el rendimiento.

## <a name="handling-device-loss"></a>Controlar la pérdida del dispositivo

Mientras se ejecuta el programa, es posible que el dispositivo gráfico que está usando no esté disponible. Por ejemplo, se puede perder el dispositivo si cambia la resolución de pantalla, o si el usuario quita el adaptador de pantalla. Si se pierde el dispositivo, el destino de representación también deja de ser válido, junto con los recursos dependientes del dispositivo asociados al dispositivo. Direct2D señala un dispositivo perdido al devolver el código de error D2DERR volver a **crear el \_ \_ destino** desde el método [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) . Si recibe este código de error, debe volver a crear el destino de representación y todos los recursos dependientes del dispositivo.

Para descartar un recurso, simplemente libere la interfaz para ese recurso.


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



La creación de un recurso puede ser una operación costosa, por lo que no se deben volver a crear los recursos de cada mensaje de [**\_ pintura de WM**](/windows/desktop/gdi/wm-paint) . Cree un recurso una vez y almacene en caché el puntero de recursos hasta que el recurso deje de ser válido debido a la pérdida del dispositivo o hasta que ya no necesite ese recurso.

## <a name="the-direct2d-render-loop"></a>El bucle de representación de Direct2D

Independientemente de lo que dibuje, el programa debe realizar un bucle similar al siguiente.

1.  Cree recursos independientes del dispositivo.
2.  Representar la escena.
    1.  Compruebe si existe un destino de representación válido. Si no es así, cree el destino de representación y los recursos dependientes del dispositivo.
    2.  Llame a [**ID2D1RenderTarget:: BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).
    3.  Emitir comandos de dibujo.
    4.  Llame a [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).
    5.  Si [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) devuelve **D2DERR \_ Recreate \_**, descarte el destino de representación y los recursos dependientes del dispositivo.
3.  Repita el paso 2 cada vez que necesite actualizar o volver a dibujar la escena.

Si el destino de representación es una ventana, el paso 2 se produce siempre que la ventana recibe un mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) .

El bucle que se muestra aquí controla la pérdida del dispositivo al descartar los recursos dependientes del dispositivo y volver a crearlos al principio del siguiente bucle (paso 2a).

## <a name="next"></a>Siguientes

[PPP y Device-Independent píxeles](dpi-and-device-independent-pixels.md)

 

 