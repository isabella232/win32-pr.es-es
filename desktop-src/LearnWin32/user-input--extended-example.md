---
<span data-ttu-id="f9ec7-101">title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="f9ec7-101">title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="user-input-extended-example"></a><span data-ttu-id="f9ec7-102">Entrada del usuario: ejemplo extendido</span><span class="sxs-lookup"><span data-stu-id="f9ec7-102">User Input: Extended Example</span></span>

<span data-ttu-id="f9ec7-103">Vamos a combinar todo lo que hemos aprendido sobre la entrada del usuario para crear un sencillo programa de dibujo.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-103">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="f9ec7-104">Esta es una captura de pantalla del programa:</span><span class="sxs-lookup"><span data-stu-id="f9ec7-104">Here is a screen shot of the program:</span></span>

![captura de pantalla del programa de dibujo](images/input03.png)

<span data-ttu-id="f9ec7-106">El usuario puede dibujar puntos suspensivos en varios colores diferentes y seleccionar, mover o eliminar puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-106">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="f9ec7-107">Para que la interfaz de usuario sea sencilla, el programa no permite al usuario seleccionar los colores de elipse.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-107">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="f9ec7-108">En su lugar, el programa pasa automáticamente por una lista predefinida de colores.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-108">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="f9ec7-109">El programa no admite formas distintas de los puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-109">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="f9ec7-110">Obviamente, este programa no ganará ningún premio por el software de gráficos.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-110">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="f9ec7-111">Sin embargo, sigue siendo un ejemplo útil del que aprender.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-111">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="f9ec7-112">Puede descargar el código fuente completo de [Ejemplo de dibujo simple](simple-drawing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f9ec7-112">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="f9ec7-113">En esta sección solo se tratarán algunos aspectos destacados.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-113">This section will just cover some highlights.</span></span>

<span data-ttu-id="f9ec7-114">Los puntos suspensivos se representan en el programa mediante una estructura que contiene los datos de elipse [**(D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) y el color ([**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)).</span><span class="sxs-lookup"><span data-stu-id="f9ec7-114">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="f9ec7-115">La estructura también define dos métodos: un método para dibujar la elipse y un método para realizar pruebas de acceso.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-115">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


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



<span data-ttu-id="f9ec7-116">El programa usa el mismo pincel de color sólido para dibujar el relleno y el contorno de cada elipse, cambiando el color según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-116">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="f9ec7-117">En Direct2D, cambiar el color de un pincel de color sólido es una operación eficaz.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-117">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="f9ec7-118">Por lo tanto, el objeto de pincel de color sólido admite un [**método SetColor.**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor)</span><span class="sxs-lookup"><span data-stu-id="f9ec7-118">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="f9ec7-119">Los puntos suspensivos se almacenan en un contenedor de lista **de** STL:</span><span class="sxs-lookup"><span data-stu-id="f9ec7-119">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="f9ec7-120">**shared \_ ptr** es una clase de puntero inteligente que se agregó a C++ en TR1 y se formalizó en C++0x.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-120">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="f9ec7-121">Visual Studio 2010 agrega compatibilidad con **\_ pt** r compartido y otras características de C++0x.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-121">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="f9ec7-122">Para obtener más información, vea [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-122">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="f9ec7-123">(Es posible que este recurso no esté disponible en algunos idiomas y países).</span><span class="sxs-lookup"><span data-stu-id="f9ec7-123">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="f9ec7-124">El programa tiene tres modos:</span><span class="sxs-lookup"><span data-stu-id="f9ec7-124">The program has three modes:</span></span>

-   <span data-ttu-id="f9ec7-125">Modo de dibujo.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-125">Draw mode.</span></span> <span data-ttu-id="f9ec7-126">El usuario puede dibujar nuevos puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-126">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="f9ec7-127">Modo de selección.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-127">Selection mode.</span></span> <span data-ttu-id="f9ec7-128">El usuario puede seleccionar una elipse.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-128">The user can select an ellipse.</span></span>
-   <span data-ttu-id="f9ec7-129">Modo de arrastre.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-129">Drag mode.</span></span> <span data-ttu-id="f9ec7-130">El usuario puede arrastrar una elipse seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-130">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="f9ec7-131">El usuario puede cambiar entre el modo de dibujo y el modo de selección mediante los mismos métodos abreviados de teclado descritos en [Tablas de aceleradores](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f9ec7-131">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="f9ec7-132">Desde el modo de selección, el programa cambia al modo de arrastre si el usuario hace clic en una elipse.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-132">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="f9ec7-133">Vuelve al modo de selección cuando el usuario suelta el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-133">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="f9ec7-134">La selección actual se almacena como un iterador en la lista de puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-134">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="f9ec7-135">El método auxiliar devuelve un puntero a la elipse seleccionada o el valor `MainWindow::Selection` **nullptr** si no hay ninguna selección.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-135">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


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



<span data-ttu-id="f9ec7-136">En la tabla siguiente se resumen los efectos de la entrada del mouse en cada uno de los tres modos.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-136">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="f9ec7-137">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="f9ec7-137">Mouse Input</span></span>      | <span data-ttu-id="f9ec7-138">Modo de dibujo</span><span class="sxs-lookup"><span data-stu-id="f9ec7-138">Draw Mode</span></span>                                          | <span data-ttu-id="f9ec7-139">Modo de selección</span><span class="sxs-lookup"><span data-stu-id="f9ec7-139">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="f9ec7-140">Modo de arrastre</span><span class="sxs-lookup"><span data-stu-id="f9ec7-140">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="f9ec7-141">Botón izquierdo hacia abajo</span><span class="sxs-lookup"><span data-stu-id="f9ec7-141">Left button down</span></span> | <span data-ttu-id="f9ec7-142">Establezca la captura del mouse y empiece a dibujar una nueva elipse.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-142">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="f9ec7-143">Libere la selección actual y realice una prueba de selección.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-143">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="f9ec7-144">Si se pulsa una elipse, capture el cursor, selecciónelo y cambie al modo de arrastre.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-144">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="f9ec7-145">No se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-145">No action.</span></span>                 |
| <span data-ttu-id="f9ec7-146">Movimiento del mouse</span><span class="sxs-lookup"><span data-stu-id="f9ec7-146">Mouse move</span></span>       | <span data-ttu-id="f9ec7-147">Si el botón izquierdo está abajo, cambie el tamaño de la elipse.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-147">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="f9ec7-148">No se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-148">No action.</span></span>                                                                                                                                   | <span data-ttu-id="f9ec7-149">Mueva la elipse seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-149">Move the selected ellipse.</span></span> |
| <span data-ttu-id="f9ec7-150">Botón izquierdo hacia arriba</span><span class="sxs-lookup"><span data-stu-id="f9ec7-150">Left button up</span></span>   | <span data-ttu-id="f9ec7-151">Deje de dibujar la elipse.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-151">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="f9ec7-152">No se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-152">No action.</span></span>                                                                                                                                   | <span data-ttu-id="f9ec7-153">Cambie al modo de selección.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-153">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="f9ec7-154">El método siguiente de la `MainWindow` clase controla los mensajes [**\_ LBUTTONDOWN de WM.**](/windows/desktop/inputdev/wm-lbuttondown)</span><span class="sxs-lookup"><span data-stu-id="f9ec7-154">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


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



<span data-ttu-id="f9ec7-155">Las coordenadas del mouse se pasan a este método en píxeles y, a continuación, se convierten en DIP.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-155">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="f9ec7-156">Es importante no confundir estas dos unidades.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-156">It is important not to confuse these two units.</span></span> <span data-ttu-id="f9ec7-157">Por ejemplo, la [**función DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) usa píxeles, pero el dibujo y las pruebas de impacto usan DIP.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-157">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="f9ec7-158">La regla general es que las funciones relacionadas con las ventanas o la entrada del mouse usan píxeles, mientras que Direct2D y DirectWrite usan DIP.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-158">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="f9ec7-159">Pruebe siempre el programa con una configuración de valores altos de PPP y recuerde marcar el programa como compatible con PPP.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-159">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="f9ec7-160">Para obtener más información, vea [PPP y Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="f9ec7-160">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="f9ec7-161">Este es el código que controla los [**mensajes \_ MOUSEMOVE de WM.**](/windows/desktop/inputdev/wm-mousemove)</span><span class="sxs-lookup"><span data-stu-id="f9ec7-161">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


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



<span data-ttu-id="f9ec7-162">La lógica para cambiar el tamaño de una elipse se describió anteriormente, en la sección [Ejemplo: Círculos de dibujo](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="f9ec7-162">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="f9ec7-163">Observe también la llamada a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="f9ec7-163">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="f9ec7-164">Esto se asegura de que la ventana se vuelva a dibujar.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-164">This makes sure that the window is repainted.</span></span> <span data-ttu-id="f9ec7-165">El código siguiente controla los [**mensajes \_ de WM LBUTTONUP.**](/windows/desktop/inputdev/wm-lbuttonup)</span><span class="sxs-lookup"><span data-stu-id="f9ec7-165">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


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



<span data-ttu-id="f9ec7-166">Como puede ver, los controladores de mensajes para la entrada del mouse tienen código de bifurcación, dependiendo del modo actual.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-166">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="f9ec7-167">Este es un diseño aceptable para este programa bastante sencillo.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-167">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="f9ec7-168">Sin embargo, podría volverse demasiado complejo si se agregan nuevos modos.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-168">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="f9ec7-169">Para un programa más grande, una arquitectura de controlador de vista de modelos (MVC) podría ser un mejor diseño.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-169">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="f9ec7-170">En este tipo de arquitectura, el *controlador*, que controla la entrada del usuario, se separa del modelo *,* que administra los datos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-170">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="f9ec7-171">Cuando el programa cambia de modo, el cursor cambia para proporcionar comentarios al usuario.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-171">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


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



<span data-ttu-id="f9ec7-172">Por último, recuerde establecer el cursor cuando la ventana reciba un [**mensaje \_ SETCURSOR de WM:**](/windows/desktop/menurc/wm-setcursor)</span><span class="sxs-lookup"><span data-stu-id="f9ec7-172">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="f9ec7-173">Resumen</span><span class="sxs-lookup"><span data-stu-id="f9ec7-173">Summary</span></span>

<span data-ttu-id="f9ec7-174">En este módulo, ha aprendido a controlar la entrada del mouse y el teclado. cómo definir métodos abreviados de teclado; y cómo actualizar la imagen del cursor para reflejar el estado actual del programa.</span><span class="sxs-lookup"><span data-stu-id="f9ec7-174">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 
