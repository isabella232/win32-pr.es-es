---
title: Movimiento del mouse
description: Movimiento del mouse
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159953"
---
# <a name="mouse-movement"></a>Movimiento del mouse

Cuando se mueve el mouse, Windows un [**mensaje WM \_ MOUSEMOVE.**](/windows/desktop/inputdev/wm-mousemove) De forma predeterminada, **WM \_ MOUSEMOVE** va a la ventana que contiene el cursor. Puede invalidar este comportamiento *capturando el* mouse, que se describe en la sección siguiente.

El [**mensaje \_ WM MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) contiene los mismos parámetros que los mensajes para los clics del mouse. Los 16 bits más bajos de *lParam* contienen la coordenada x y los 16 bits siguientes contienen la coordenada y. Use las macros [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) [**y GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para desempaquetar las coordenadas *de lParam.* El *parámetro wParam* contiene un **OR** bit a bit de marcas, que indica el estado de los demás botones del mouse más las teclas MAYÚS y CTRL. El código siguiente obtiene las coordenadas del mouse *de lParam*.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Recuerde que estas coordenadas están en píxeles, no en píxeles independientes del dispositivo (DIP). Más adelante en este tema, se verá el código que convierte entre las dos unidades.

Una ventana también puede recibir un [**mensaje \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) de WM si la posición del cursor cambia con respecto a la ventana. Por ejemplo, si el cursor se coloca sobre una ventana y el usuario oculta la ventana, la ventana recibe mensajes **\_ WM MOUSEMOVE** incluso si el mouse no se movió. Una consecuencia de este comportamiento es que es posible que las coordenadas del mouse no cambien entre **los mensajes DE WM \_ MOUSEMOVE.**

## <a name="capturing-mouse-movement-outside-the-window"></a>Captura del movimiento del mouse fuera de la ventana

De forma predeterminada, una ventana deja de recibir [**mensajes \_ WM MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) si el mouse se mueve más allá del borde del área cliente. Sin embargo, para algunas operaciones, es posible que tenga que realizar un seguimiento de la posición del mouse más allá de este punto. Por ejemplo, un programa de dibujo podría permitir al usuario arrastrar el rectángulo de selección más allá del borde de la ventana, como se muestra en el diagrama siguiente.

![ilustración de la captura del mouse.](images/input01.png)

Para recibir mensajes de movimiento del mouse más allá del borde de la ventana, llame a la [**función SetCapture.**](/windows/desktop/api/winuser/nf-winuser-setcapture) Después de llamar a esta función, la ventana seguirá recibiendo mensajes [**\_ WM MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) mientras el usuario mantenga presionado al menos un botón del mouse, incluso si el mouse se mueve fuera de la ventana. La ventana de captura debe ser la ventana de primer plano y solo una ventana puede ser la ventana de captura a la vez. Para liberar la captura del mouse, llame a [**la función ReleaseCapture.**](/windows/desktop/api/winuser/nf-winuser-releasecapture)

Normalmente, usaría [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) y [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) de la siguiente manera.

1.  Cuando el usuario presione el botón izquierdo del mouse, llame a [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) para empezar a capturar el mouse.
2.  Responder a mensajes de movimiento del mouse.
3.  Cuando el usuario suelte el botón izquierdo del mouse, llame a [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).

## <a name="example-drawing-circles"></a>Ejemplo: Dibujar círculos

Vamos a ampliar el programa Círculo del [módulo 3](module-3---windows-graphics.md) al permitir que el usuario dibuje un círculo con el mouse. Comience con el [programa Ejemplo de círculo de Direct2D.](direct2d-circle-sample.md) Modificaremos el código de este ejemplo para agregar un dibujo simple. En primer lugar, agregue una nueva variable miembro a la `MainWindow` clase .


```C++
    D2D1_POINT_2F           ptMouse;
```



Esta variable almacena la posición del mouse hacia abajo mientras el usuario arrastra el mouse. En el `MainWindow` constructor, inicialice las variables *ellipse* *y ptMouse.*


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



Quite el cuerpo del `MainWindow::CalculateLayout` método; no es necesario para este ejemplo.


```C++
    void    CalculateLayout() { }
```



A continuación, declare controladores de mensajes para los mensajes del botón izquierdo hacia abajo, el botón izquierdo hacia arriba y el movimiento del mouse.


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



Las coordenadas del mouse se dan en píxeles físicos, pero Direct2D espera píxeles independientes del dispositivo (DIP). Para controlar correctamente la configuración de valores altos de PPP, debe traducir las coordenadas de píxel en DIP. Para obtener más información sobre PPP, vea [PPP y Device-Independent Pixels](dpi-and-device-independent-pixels.md). En el código siguiente se muestra una clase auxiliar que convierte píxeles en DIP.


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



Llame `DPIScale::Initialize` a en el controlador WM [**\_ CREATE**](/windows/desktop/winmsg/wm-create) después de crear el objeto de generador de Direct2D.


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



Para obtener las coordenadas del mouse en DIP a partir de los mensajes del mouse, haga lo siguiente:

1.  Use las macros [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) [**y GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) para obtener las coordenadas de píxel. Estas macros se definen en WindowsX.h, por lo que no olvide incluir ese encabezado en el proyecto.
2.  Llame `DPIScale::PixelsToDipsX` a y para convertir `DPIScale::PixelsToDipsY` píxeles en DIP.

Ahora agregue los controladores de mensajes al procedimiento de ventana.


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



Por último, implemente los propios controladores de mensajes.

### <a name="left-button-down"></a>Botón izquierdo hacia abajo

Para el mensaje de abajo del botón izquierdo, haga lo siguiente:

1.  Llame [**a SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) para empezar a capturar el mouse.
2.  Almacene la posición del clic del mouse en la variable *ptMouse.* Esta posición define la esquina superior izquierda del cuadro de límite para la elipse.
3.  Restablezca la estructura de puntos suspensivos.
4.  Llame [**a InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Esta función obliga a que se vuelva a dibujar la ventana.


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a>Mover el mouse

Para el mensaje de movimiento del mouse, compruebe si el botón izquierdo del mouse está apagado. Si es así, vuelva a calcular la elipse y vuelva a dibujar la ventana. En Direct2D, una elipse se define mediante el punto central y x e y-radii. Queremos dibujar una elipse que se ajuste al rectángulo delimitador definido por el punto de desplazamiento del mouse *(ptMouse)* y la posición actual del cursor *(x*, *y*), por lo que se necesita un poco de aritmética para encontrar el ancho, el alto y la posición de la elipse.

El código siguiente vuelve a calcular la elipse y, a continuación, llama a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) para volver a dibujar la ventana.

![Diagrama que muestra una elipse con radios x e y.](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a>Botón izquierdo hacia arriba

Para el mensaje de botón izquierdo hacia arriba, simplemente llame a [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) para liberar la captura del mouse.


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a>Siguientes

[Otras operaciones del mouse](other-mouse-operations.md)

 

 