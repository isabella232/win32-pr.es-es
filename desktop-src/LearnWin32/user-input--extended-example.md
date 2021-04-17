---
title: Ejemplo de entrada extendida de usuario
description: .
ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdde7f14dda356d0f65103c77e3b73c2f0de50a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104559167"
---
# <a name="user-input-extended-example"></a><span data-ttu-id="5c933-103">Entrada de usuario: ejemplo extendido</span><span class="sxs-lookup"><span data-stu-id="5c933-103">User Input: Extended Example</span></span>

<span data-ttu-id="5c933-104">Vamos a combinar todo lo que hemos aprendido sobre los datos proporcionados por el usuario para crear un programa de dibujo sencillo.</span><span class="sxs-lookup"><span data-stu-id="5c933-104">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="5c933-105">Esta es una captura de pantalla del programa:</span><span class="sxs-lookup"><span data-stu-id="5c933-105">Here is a screen shot of the program:</span></span>

![captura de pantalla del programa de dibujo](images/input03.png)

<span data-ttu-id="5c933-107">El usuario puede dibujar puntos suspensivos en varios colores diferentes y seleccionar, desplace o eliminar puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="5c933-107">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="5c933-108">Para mantener la interfaz de usuario sencilla, el programa no permite al usuario seleccionar los colores de la elipse.</span><span class="sxs-lookup"><span data-stu-id="5c933-108">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="5c933-109">En su lugar, el programa recorre automáticamente una lista predefinida de colores.</span><span class="sxs-lookup"><span data-stu-id="5c933-109">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="5c933-110">El programa no admite formas que no sean puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="5c933-110">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="5c933-111">Obviamente, este programa no ganará ningún premio por el software de gráficos.</span><span class="sxs-lookup"><span data-stu-id="5c933-111">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="5c933-112">Sin embargo, sigue siendo un ejemplo útil para aprender de.</span><span class="sxs-lookup"><span data-stu-id="5c933-112">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="5c933-113">Puede descargar el código fuente completo desde el [ejemplo de dibujo sencillo](simple-drawing-sample.md).</span><span class="sxs-lookup"><span data-stu-id="5c933-113">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="5c933-114">En esta sección solo se tratarán algunos aspectos destacados.</span><span class="sxs-lookup"><span data-stu-id="5c933-114">This section will just cover some highlights.</span></span>

<span data-ttu-id="5c933-115">Los puntos suspensivos se representan en el programa mediante una estructura que contiene los datos de la elipse ([**D2D1 \_ Ellipse**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) y el color ([**D2D1 \_ color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)).</span><span class="sxs-lookup"><span data-stu-id="5c933-115">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="5c933-116">La estructura también define dos métodos: un método para dibujar la elipse y un método para realizar la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="5c933-116">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


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



<span data-ttu-id="5c933-117">El programa usa el mismo pincel de color sólido para dibujar el relleno y el contorno de cada elipse, cambiando el color según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="5c933-117">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="5c933-118">En Direct2D, cambiar el color de un pincel de color sólido es una operación eficaz.</span><span class="sxs-lookup"><span data-stu-id="5c933-118">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="5c933-119">Por lo tanto, el objeto de pincel de color sólido admite un método [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) .</span><span class="sxs-lookup"><span data-stu-id="5c933-119">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="5c933-120">Los puntos suspensivos se almacenan en un contenedor de **lista** STL:</span><span class="sxs-lookup"><span data-stu-id="5c933-120">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="5c933-121">**\_ ptr compartido** es una clase de puntero inteligente que se agregó a C++ en TR1 y se formalizó en C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="5c933-121">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="5c933-122">Visual Studio 2010 agrega compatibilidad con las características **compartidas de \_ PT** r y otras funciones de C + + 0x.</span><span class="sxs-lookup"><span data-stu-id="5c933-122">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="5c933-123">Para obtener más información, vea [explorar nuevas características de C++ y MFC en Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) en *MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="5c933-123">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="5c933-124">(Es posible que este recurso no esté disponible en algunos idiomas y países).</span><span class="sxs-lookup"><span data-stu-id="5c933-124">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="5c933-125">El programa tiene tres modos:</span><span class="sxs-lookup"><span data-stu-id="5c933-125">The program has three modes:</span></span>

-   <span data-ttu-id="5c933-126">Modo Draw.</span><span class="sxs-lookup"><span data-stu-id="5c933-126">Draw mode.</span></span> <span data-ttu-id="5c933-127">El usuario puede dibujar nuevos puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="5c933-127">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="5c933-128">Modo de selección.</span><span class="sxs-lookup"><span data-stu-id="5c933-128">Selection mode.</span></span> <span data-ttu-id="5c933-129">El usuario puede seleccionar una elipse.</span><span class="sxs-lookup"><span data-stu-id="5c933-129">The user can select an ellipse.</span></span>
-   <span data-ttu-id="5c933-130">Modo de arrastre.</span><span class="sxs-lookup"><span data-stu-id="5c933-130">Drag mode.</span></span> <span data-ttu-id="5c933-131">El usuario puede arrastrar una elipse seleccionada.</span><span class="sxs-lookup"><span data-stu-id="5c933-131">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="5c933-132">El usuario puede cambiar entre el modo de dibujo y el modo de selección utilizando los mismos métodos abreviados de teclado descritos en [las tablas de aceleradores](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5c933-132">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="5c933-133">En el modo de selección, el programa cambia al modo de arrastre Si el usuario hace clic en una elipse.</span><span class="sxs-lookup"><span data-stu-id="5c933-133">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="5c933-134">Vuelve al modo de selección cuando el usuario suelta el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="5c933-134">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="5c933-135">La selección actual se almacena como un iterador en la lista de puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="5c933-135">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="5c933-136">El método auxiliar `MainWindow::Selection` devuelve un puntero a la elipse seleccionada o el valor **nullptr** si no hay ninguna selección.</span><span class="sxs-lookup"><span data-stu-id="5c933-136">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


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



<span data-ttu-id="5c933-137">En la tabla siguiente se resumen los efectos de la entrada del mouse en cada uno de los tres modos.</span><span class="sxs-lookup"><span data-stu-id="5c933-137">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="5c933-138">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="5c933-138">Mouse Input</span></span>      | <span data-ttu-id="5c933-139">Modo de dibujo</span><span class="sxs-lookup"><span data-stu-id="5c933-139">Draw Mode</span></span>                                          | <span data-ttu-id="5c933-140">Modo de selección</span><span class="sxs-lookup"><span data-stu-id="5c933-140">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="5c933-141">Modo de arrastre</span><span class="sxs-lookup"><span data-stu-id="5c933-141">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="5c933-142">Botón primario abajo</span><span class="sxs-lookup"><span data-stu-id="5c933-142">Left button down</span></span> | <span data-ttu-id="5c933-143">Establezca la captura del mouse y empiece a dibujar una nueva elipse.</span><span class="sxs-lookup"><span data-stu-id="5c933-143">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="5c933-144">Libera la selección actual y realiza una prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="5c933-144">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="5c933-145">Si se alcanza una elipse, Capture el cursor, seleccione la elipse y cambie al modo de arrastre.</span><span class="sxs-lookup"><span data-stu-id="5c933-145">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="5c933-146">No se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="5c933-146">No action.</span></span>                 |
| <span data-ttu-id="5c933-147">Movimiento del mouse</span><span class="sxs-lookup"><span data-stu-id="5c933-147">Mouse move</span></span>       | <span data-ttu-id="5c933-148">Si el botón izquierdo está inactivo, cambie el tamaño de la elipse.</span><span class="sxs-lookup"><span data-stu-id="5c933-148">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="5c933-149">No se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="5c933-149">No action.</span></span>                                                                                                                                   | <span data-ttu-id="5c933-150">Mueve la elipse seleccionada.</span><span class="sxs-lookup"><span data-stu-id="5c933-150">Move the selected ellipse.</span></span> |
| <span data-ttu-id="5c933-151">Botón primario arriba</span><span class="sxs-lookup"><span data-stu-id="5c933-151">Left button up</span></span>   | <span data-ttu-id="5c933-152">Detiene el dibujo de la elipse.</span><span class="sxs-lookup"><span data-stu-id="5c933-152">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="5c933-153">No se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="5c933-153">No action.</span></span>                                                                                                                                   | <span data-ttu-id="5c933-154">Cambiar al modo de selección.</span><span class="sxs-lookup"><span data-stu-id="5c933-154">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="5c933-155">El método siguiente de la `MainWindow` clase controla los mensajes de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) .</span><span class="sxs-lookup"><span data-stu-id="5c933-155">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


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



<span data-ttu-id="5c933-156">Las coordenadas del mouse se pasan a este método en píxeles y, a continuación, se convierten en DIP.</span><span class="sxs-lookup"><span data-stu-id="5c933-156">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="5c933-157">Es importante no confundir estas dos unidades.</span><span class="sxs-lookup"><span data-stu-id="5c933-157">It is important not to confuse these two units.</span></span> <span data-ttu-id="5c933-158">Por ejemplo, la función [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) usa píxeles, pero el dibujo y la prueba de posicionamiento usan DIP.</span><span class="sxs-lookup"><span data-stu-id="5c933-158">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="5c933-159">La regla general es que las funciones relacionadas con la entrada de mouse o Windows usan píxeles, mientras que Direct2D y DirectWrite usan DIP.</span><span class="sxs-lookup"><span data-stu-id="5c933-159">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="5c933-160">Pruebe siempre el programa con un valor de PPP alto y recuerde marcar el programa como compatible con PPP.</span><span class="sxs-lookup"><span data-stu-id="5c933-160">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="5c933-161">Para obtener más información, vea [PPP y Device-Independent píxeles](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="5c933-161">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="5c933-162">Este es el código que controla los mensajes de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="5c933-162">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


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



<span data-ttu-id="5c933-163">La lógica para cambiar el tamaño de una elipse se ha descrito anteriormente, en la sección [ejemplo: dibujo de círculos](mouse-movement.md).</span><span class="sxs-lookup"><span data-stu-id="5c933-163">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="5c933-164">Observe también la llamada a [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="5c933-164">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="5c933-165">Esto garantiza que la ventana se vuelva a dibujar.</span><span class="sxs-lookup"><span data-stu-id="5c933-165">This makes sure that the window is repainted.</span></span> <span data-ttu-id="5c933-166">El código siguiente controla los mensajes de [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="5c933-166">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


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



<span data-ttu-id="5c933-167">Como puede ver, los controladores de mensajes para la entrada del mouse tienen el código de bifurcación, dependiendo del modo actual.</span><span class="sxs-lookup"><span data-stu-id="5c933-167">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="5c933-168">Este es un diseño aceptable para este programa bastante sencillo.</span><span class="sxs-lookup"><span data-stu-id="5c933-168">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="5c933-169">Sin embargo, podría ser demasiado complejo si se agregan nuevos modos.</span><span class="sxs-lookup"><span data-stu-id="5c933-169">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="5c933-170">Para un programa más grande, una arquitectura de modelo-vista-controlador (MVC) podría ser un mejor diseño.</span><span class="sxs-lookup"><span data-stu-id="5c933-170">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="5c933-171">En este tipo de arquitectura, el *controlador*, que controla la entrada del usuario, está separado del *modelo*, que administra los datos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5c933-171">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="5c933-172">Cuando el programa cambia de modo, el cursor cambia para proporcionar comentarios al usuario.</span><span class="sxs-lookup"><span data-stu-id="5c933-172">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


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



<span data-ttu-id="5c933-173">Y, por último, no olvide establecer el cursor cuando la ventana reciba un mensaje de [**\_ SETCURSOR de WM**](/windows/desktop/menurc/wm-setcursor) :</span><span class="sxs-lookup"><span data-stu-id="5c933-173">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="5c933-174">Resumen</span><span class="sxs-lookup"><span data-stu-id="5c933-174">Summary</span></span>

<span data-ttu-id="5c933-175">En este módulo, aprendió a controlar la entrada del mouse y del teclado. Cómo definir los métodos abreviados de teclado; y cómo actualizar la imagen del cursor para reflejar el estado actual del programa.</span><span class="sxs-lookup"><span data-stu-id="5c933-175">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 