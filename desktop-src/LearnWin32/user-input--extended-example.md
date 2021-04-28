---
title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018
---

# <a name="user-input-extended-example"></a>Entrada del usuario: ejemplo extendido

Vamos a combinar todo lo que hemos aprendido sobre la entrada del usuario para crear un sencillo programa de dibujo. Esta es una captura de pantalla del programa:

![captura de pantalla del programa de dibujo](images/input03.png)

El usuario puede dibujar puntos suspensivos en varios colores diferentes y seleccionar, mover o eliminar puntos suspensivos. Para que la interfaz de usuario sea sencilla, el programa no permite al usuario seleccionar los colores de elipse. En su lugar, el programa pasa automáticamente por una lista predefinida de colores. El programa no admite formas distintas de los puntos suspensivos. Obviamente, este programa no ganará ningún premio por el software de gráficos. Sin embargo, sigue siendo un ejemplo útil del que aprender. Puede descargar el código fuente completo de [Ejemplo de dibujo simple](simple-drawing-sample.md). En esta sección solo se tratarán algunos aspectos destacados.

Los puntos suspensivos se representan en el programa mediante una estructura que contiene los datos de elipse [**(D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) y el color ([**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)). La estructura también define dos métodos: un método para dibujar la elipse y un método para realizar pruebas de acceso.


```C++
struct MyEllipse
{
    D2D1_ELLIPSE    ellipse;
    D2D1_COLOR_F    color;

    void Draw(ID2D1RenderTarget *pRT, ID2D1SolidColorBrush *pBrush)
    {
        pBrush->SetColor(color);
        pRT->FillEllipse(ellipse, pBrush);
        pBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black));
        pRT->DrawEllipse(ellipse, pBrush, 1.0f);
    }

    BOOL HitTest(float x, float y)
    {
        const float a = ellipse.radiusX;
        const float b = ellipse.radiusY;
        const float x1 = x - ellipse.point.x;
        const float y1 = y - ellipse.point.y;
        const float d = ((x1 * x1) / (a * a)) + ((y1 * y1) / (b * b));
        return d <= 1.0f;
    }
};
```



El programa usa el mismo pincel de color sólido para dibujar el relleno y el contorno de cada elipse, cambiando el color según sea necesario. En Direct2D, cambiar el color de un pincel de color sólido es una operación eficaz. Por lo tanto, el objeto de pincel de color sólido admite un [**método SetColor.**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor)

Los puntos suspensivos se almacenan en un contenedor de lista **de** STL:


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **shared \_ ptr** es una clase de puntero inteligente que se agregó a C++ en TR1 y se formalizó en C++0x. Visual Studio 2010 agrega compatibilidad con **\_ pt** r compartido y otras características de C++0x. Para obtener más información, vea [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*. (Es posible que este recurso no esté disponible en algunos idiomas y países).

 

El programa tiene tres modos:

-   Modo de dibujo. El usuario puede dibujar nuevos puntos suspensivos.
-   Modo de selección. El usuario puede seleccionar una elipse.
-   Modo de arrastre. El usuario puede arrastrar una elipse seleccionada.

El usuario puede cambiar entre el modo de dibujo y el modo de selección mediante los mismos métodos abreviados de teclado descritos en [Tablas de aceleradores](accelerator-tables.md). Desde el modo de selección, el programa cambia al modo de arrastre si el usuario hace clic en una elipse. Vuelve al modo de selección cuando el usuario suelta el botón del mouse. La selección actual se almacena como un iterador en la lista de puntos suspensivos. El método auxiliar devuelve un puntero a la elipse seleccionada o el valor `MainWindow::Selection` **nullptr** si no hay ninguna selección.


```C++
    list<shared_ptr<MyEllipse>>::iterator   selection;
     
    shared_ptr<MyEllipse> Selection() 
    { 
        if (selection == ellipses.end()) 
        { 
            return nullptr;
        }
        else
        {
            return (*selection);
        }
    }

    void    ClearSelection() { selection = ellipses.end(); }
```



En la tabla siguiente se resumen los efectos de la entrada del mouse en cada uno de los tres modos.



| Entrada del mouse      | Modo de dibujo                                          | Modo de selección                                                                                                                               | Modo de arrastre                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Botón izquierdo hacia abajo | Establezca la captura del mouse y empiece a dibujar una nueva elipse. | Libere la selección actual y realice una prueba de selección. Si se pulsa una elipse, capture el cursor, selecciónelo y cambie al modo de arrastre. | No se requiere ninguna acción.                 |
| Movimiento del mouse       | Si el botón izquierdo está abajo, cambie el tamaño de la elipse.    | No se requiere ninguna acción.                                                                                                                                   | Mueva la elipse seleccionada. |
| Botón izquierdo hacia arriba   | Deje de dibujar la elipse.                          | No se requiere ninguna acción.                                                                                                                                   | Cambie al modo de selección.  |



 

El método siguiente de la `MainWindow` clase controla los mensajes [**\_ LBUTTONDOWN de WM.**](/windows/desktop/inputdev/wm-lbuttondown)


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if (mode == DrawMode)
    {
        POINT pt = { pixelX, pixelY };

        if (DragDetect(m_hwnd, pt))
        {
            SetCapture(m_hwnd);
        
            // Start a new ellipse.
            InsertEllipse(dipX, dipY);
        }
    }
    else
    {
        ClearSelection();

        if (HitTest(dipX, dipY))
        {
            SetCapture(m_hwnd);

            ptMouse = Selection()->ellipse.point;
            ptMouse.x -= dipX;
            ptMouse.y -= dipY;

            SetMode(DragMode);
        }
    }
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



Las coordenadas del mouse se pasan a este método en píxeles y, a continuación, se convierten en DIP. Es importante no confundir estas dos unidades. Por ejemplo, la [**función DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) usa píxeles, pero el dibujo y las pruebas de impacto usan DIP. La regla general es que las funciones relacionadas con las ventanas o la entrada del mouse usan píxeles, mientras que Direct2D y DirectWrite usan DIP. Pruebe siempre el programa con una configuración de valores altos de PPP y recuerde marcar el programa como compatible con PPP. Para obtener más información, vea [PPP y Device-Independent Pixels](dpi-and-device-independent-pixels.md).

Este es el código que controla los [**mensajes \_ MOUSEMOVE de WM.**](/windows/desktop/inputdev/wm-mousemove)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if ((flags & MK_LBUTTON) && Selection())
    { 
        if (mode == DrawMode)
        {
            // Resize the ellipse.
            const float width = (dipX - ptMouse.x) / 2;
            const float height = (dipY - ptMouse.y) / 2;
            const float x1 = ptMouse.x + width;
            const float y1 = ptMouse.y + height;

            Selection()->ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);
        }
        else if (mode == DragMode)
        {
            // Move the ellipse.
            Selection()->ellipse.point.x = dipX + ptMouse.x;
            Selection()->ellipse.point.y = dipY + ptMouse.y;
        }
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



La lógica para cambiar el tamaño de una elipse se describió anteriormente, en la sección [Ejemplo: Círculos de dibujo](mouse-movement.md). Observe también la llamada a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Esto se asegura de que la ventana se vuelva a dibujar. El código siguiente controla los [**mensajes \_ de WM LBUTTONUP.**](/windows/desktop/inputdev/wm-lbuttonup)


```C++
void MainWindow::OnLButtonUp()
{
    if ((mode == DrawMode) && Selection())
    {
        ClearSelection();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
    else if (mode == DragMode)
    {
        SetMode(SelectMode);
    }
    ReleaseCapture(); 
}
```



Como puede ver, los controladores de mensajes para la entrada del mouse tienen código de bifurcación, dependiendo del modo actual. Este es un diseño aceptable para este programa bastante sencillo. Sin embargo, podría volverse demasiado complejo si se agregan nuevos modos. Para un programa más grande, una arquitectura de controlador de vista de modelos (MVC) podría ser un mejor diseño. En este tipo de arquitectura, el *controlador*, que controla la entrada del usuario, se separa del modelo *,* que administra los datos de la aplicación.

Cuando el programa cambia de modo, el cursor cambia para proporcionar comentarios al usuario.


```C++
void MainWindow::SetMode(Mode m)
{
    mode = m;

    // Update the cursor
    LPWSTR cursor;
    switch (mode)
    {
    case DrawMode:
        cursor = IDC_CROSS;
        break;

    case SelectMode:
        cursor = IDC_HAND;
        break;

    case DragMode:
        cursor = IDC_SIZEALL;
        break;
    }

    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
}
```



Por último, recuerde establecer el cursor cuando la ventana reciba un [**mensaje \_ SETCURSOR de WM:**](/windows/desktop/menurc/wm-setcursor)


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a>Resumen

En este módulo, ha aprendido a controlar la entrada del mouse y el teclado. cómo definir métodos abreviados de teclado; y cómo actualizar la imagen del cursor para reflejar el estado actual del programa.

 

 
