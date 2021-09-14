---
title: Dibujo con Direct2D
description: Después de crear los recursos gráficos, está listo para dibujar.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159987"
---
# <a name="drawing-with-direct2d"></a>Dibujo con Direct2D

Después de crear los recursos gráficos, está listo para dibujar.

## <a name="drawing-an-ellipse"></a>Dibujar una elipse

El [programa Circle](your-first-direct2d-program.md) realiza una lógica de dibujo muy sencilla:

1.  Rellene el fondo con un color sólido.
2.  Dibuje un círculo relleno.

![una captura de pantalla del programa de círculo.](images/graphics08.png)

Dado que el destino de representación es una ventana (en lugar de un mapa de bits u otra superficie fuera de pantalla), el dibujo se realiza en respuesta a los [**mensajes \_ WM PAINT.**](/windows/desktop/gdi/wm-paint) El código siguiente muestra el procedimiento de ventana para el programa Circle.


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



La [**interfaz ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) se usa para todas las operaciones de dibujo. El método del `OnPaint` programa hace lo siguiente:

1.  El [**método ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) indica el inicio del dibujo.
2.  El [**método ID2D1RenderTarget::Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) rellena todo el destino de representación con un color sólido. El color se da como una [**estructura D2D1 \_ COLOR \_ F.**](/windows/desktop/Direct2D/d2d1-color-f) Puede usar la [**clase D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) para inicializar la estructura. Para obtener más información, [vea Usar color en Direct2D.](using-color-in-direct2d.md)
3.  El [**método ID2D1RenderTarget::FillPxpse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dibuja una elipse rellena, usando el pincel especificado para el relleno. Una elipse se especifica mediante un punto central y los radios x e y. Si los radios x e y son iguales, el resultado es un círculo.
4.  El [**método ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) indica la finalización del dibujo para este marco. Todas las operaciones de dibujo deben realizarse entre las llamadas [**a BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) **y EndDraw.**

Los [**métodos BeginDraw,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)y [**FillVelopse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) tienen un tipo de valor devuelto **void.** Si se produce un error durante la ejecución de cualquiera de estos métodos, el error se señala a través del valor devuelto del [**método EndDraw.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) El `CreateGraphicsResources` método se muestra en el tema Creating [Direct2D Resources](render-targets--devices--and-resources.md). Este método crea el destino de representación y el pincel de color sólido.

El dispositivo podría almacenar en búfer los comandos de dibujo y aplazarlos hasta que se llame a [**EndDraw.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Puede forzar al dispositivo a ejecutar los comandos de dibujo pendientes llamando a [**ID2D1RenderTarget::Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush). Sin embargo, el vaciado puede reducir el rendimiento.

## <a name="handling-device-loss"></a>Control de la pérdida de dispositivos

Mientras se ejecuta el programa, es posible que el dispositivo gráfico que usa no esté disponible. Por ejemplo, el dispositivo se puede perder si cambia la resolución de pantalla o si el usuario quita el adaptador de pantalla. Si se pierde el dispositivo, el destino de representación también deja de ser válido, junto con los recursos dependientes del dispositivo asociados al dispositivo. Direct2D señala un dispositivo perdido devolviendo el código de error **D2DERR \_ RECREATE \_ TARGET** desde [**el método EndDraw.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) Si recibe este código de error, debe volver a crear el destino de representación y todos los recursos dependientes del dispositivo.

Para descartar un recurso, simplemente libere la interfaz de ese recurso.


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



La creación de un recurso puede ser una operación costosa, por lo que no vuelva a crear los recursos para cada [**mensaje \_ DE WM PAINT.**](/windows/desktop/gdi/wm-paint) Cree un recurso una vez y almacenar en caché el puntero de recurso hasta que el recurso no sea válido debido a la pérdida del dispositivo o hasta que ya no necesite ese recurso.

## <a name="the-direct2d-render-loop"></a>Bucle de representación de Direct2D

Independientemente de lo que dibuje, el programa debe realizar un bucle similar al siguiente.

1.  Cree recursos independientes del dispositivo.
2.  Represente la escena.
    1.  Compruebe si existe un destino de representación válido. Si no es así, cree el destino de representación y los recursos dependientes del dispositivo.
    2.  Llame [**a ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).
    3.  Emitir comandos de dibujo.
    4.  Llame [**a ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).
    5.  Si [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) devuelve **D2DERR \_ RECREATE \_ TARGET,** descarte el destino de representación y los recursos dependientes del dispositivo.
3.  Repita el paso 2 siempre que necesite actualizar o volver a dibujar la escena.

Si el destino de representación es una ventana, el paso 2 se produce cada vez que la ventana recibe un [**mensaje \_ WM PAINT.**](/windows/desktop/gdi/wm-paint)

El bucle que se muestra aquí controla la pérdida de dispositivos al descartar los recursos dependientes del dispositivo y volver a crearlos al principio del bucle siguiente (paso 2a).

## <a name="next"></a>Siguientes

[PPP y Device-Independent píxeles](dpi-and-device-independent-pixels.md)

 

 