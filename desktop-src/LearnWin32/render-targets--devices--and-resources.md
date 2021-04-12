---
title: Destinos de representación, dispositivos y recursos
description: Destinos de representación, dispositivos y recursos
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358905"
---
# <a name="render-targets-devices-and-resources"></a><span data-ttu-id="4bce8-103">Destinos de representación, dispositivos y recursos</span><span class="sxs-lookup"><span data-stu-id="4bce8-103">Render Targets, Devices, and Resources</span></span>

<span data-ttu-id="4bce8-104">Un *destino de representación* es simplemente la ubicación donde se dibujará el programa.</span><span class="sxs-lookup"><span data-stu-id="4bce8-104">A *render target* is simply the location where your program will draw.</span></span> <span data-ttu-id="4bce8-105">Normalmente, el destino de representación es una ventana (concretamente, el área cliente de la ventana).</span><span class="sxs-lookup"><span data-stu-id="4bce8-105">Typically, the render target is a window (specifically, the client area of the window).</span></span> <span data-ttu-id="4bce8-106">También podría ser un mapa de bits en memoria que no se muestra.</span><span class="sxs-lookup"><span data-stu-id="4bce8-106">It could also be a bitmap in memory that is not displayed.</span></span> <span data-ttu-id="4bce8-107">Un destino de representación se representa mediante la interfaz [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="4bce8-107">A render target is represented by the [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span>

<span data-ttu-id="4bce8-108">Un *dispositivo* es una abstracción que representa lo que realmente dibuja los píxeles.</span><span class="sxs-lookup"><span data-stu-id="4bce8-108">A *device* is an abstraction that represents whatever actually draws the pixels.</span></span> <span data-ttu-id="4bce8-109">Un dispositivo de hardware usa la GPU para obtener un rendimiento más rápido, mientras que un dispositivo de software usa la CPU.</span><span class="sxs-lookup"><span data-stu-id="4bce8-109">A hardware device uses the GPU for faster performance, whereas a software device uses the CPU.</span></span> <span data-ttu-id="4bce8-110">La aplicación no crea el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bce8-110">The application does not create the device.</span></span> <span data-ttu-id="4bce8-111">En su lugar, el dispositivo se crea implícitamente cuando la aplicación crea el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4bce8-111">Instead, the device is created implicitly when the application creates the render target.</span></span> <span data-ttu-id="4bce8-112">Cada destino de representación está asociado a un dispositivo determinado, ya sea hardware o software.</span><span class="sxs-lookup"><span data-stu-id="4bce8-112">Each render target is associated with a particular device, either hardware or software.</span></span>

![diagrama que muestra la relación entre un destino de representación y un dispositivo.](images/graphics09.png)

<span data-ttu-id="4bce8-114">Un *recurso* es un objeto que el programa utiliza para dibujar.</span><span class="sxs-lookup"><span data-stu-id="4bce8-114">A *resource* is an object that the program uses for drawing.</span></span> <span data-ttu-id="4bce8-115">Estos son algunos ejemplos de recursos que se definen en Direct2D:</span><span class="sxs-lookup"><span data-stu-id="4bce8-115">Here are some examples of resources that are defined in Direct2D:</span></span>

-   <span data-ttu-id="4bce8-116">**Pincel**.</span><span class="sxs-lookup"><span data-stu-id="4bce8-116">**Brush**.</span></span> <span data-ttu-id="4bce8-117">Controla cómo se dibujan las líneas y las regiones.</span><span class="sxs-lookup"><span data-stu-id="4bce8-117">Controls how lines and regions are painted.</span></span> <span data-ttu-id="4bce8-118">Los tipos de pincel incluyen pinceles de color sólido y pinceles de degradado.</span><span class="sxs-lookup"><span data-stu-id="4bce8-118">Brush types include solid-color brushes and gradient brushes.</span></span>
-   <span data-ttu-id="4bce8-119">**Estilo de trazo**.</span><span class="sxs-lookup"><span data-stu-id="4bce8-119">**Stroke style**.</span></span> <span data-ttu-id="4bce8-120">Controla la apariencia de una línea, por ejemplo, discontinua o Solid.</span><span class="sxs-lookup"><span data-stu-id="4bce8-120">Controls the appearance of a line—for example, dashed or solid.</span></span>
-   <span data-ttu-id="4bce8-121">**Geometría**.</span><span class="sxs-lookup"><span data-stu-id="4bce8-121">**Geometry**.</span></span> <span data-ttu-id="4bce8-122">Representa una colección de líneas y curvas.</span><span class="sxs-lookup"><span data-stu-id="4bce8-122">Represents a collection of lines and curves.</span></span>
-   <span data-ttu-id="4bce8-123">**Malla**.</span><span class="sxs-lookup"><span data-stu-id="4bce8-123">**Mesh**.</span></span> <span data-ttu-id="4bce8-124">Forma formada por triángulos.</span><span class="sxs-lookup"><span data-stu-id="4bce8-124">A shape formed out of triangles.</span></span> <span data-ttu-id="4bce8-125">Los datos de malla se pueden usar directamente en la GPU, a diferencia de los datos de geometría, que se deben convertir antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="4bce8-125">Mesh data can be consumed directly by the GPU, unlike geometry data, which must be converted before rendering.</span></span>

<span data-ttu-id="4bce8-126">Los destinos de representación también se consideran un tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="4bce8-126">Render targets are also considered a type of resource.</span></span>

<span data-ttu-id="4bce8-127">Algunos recursos se benefician de la aceleración de hardware.</span><span class="sxs-lookup"><span data-stu-id="4bce8-127">Some resources benefit from hardware acceleration.</span></span> <span data-ttu-id="4bce8-128">Un recurso de este tipo siempre está asociado a un dispositivo determinado, ya sea hardware (GPU) o software (CPU).</span><span class="sxs-lookup"><span data-stu-id="4bce8-128">A resource of this type is always associated with a particular device, either hardware (GPU) or software (CPU).</span></span> <span data-ttu-id="4bce8-129">Este tipo de recurso se denomina *dependiente del dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="4bce8-129">This type of resource is called *device-dependent*.</span></span> <span data-ttu-id="4bce8-130">Los pinceles y las mallas son ejemplos de recursos dependientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bce8-130">Brushes and meshes are examples of device-dependent resources.</span></span> <span data-ttu-id="4bce8-131">Si el dispositivo deja de estar disponible, se debe volver a crear el recurso para un dispositivo nuevo.</span><span class="sxs-lookup"><span data-stu-id="4bce8-131">If the device becomes unavailable, the resource must be re-created for a new device.</span></span>

<span data-ttu-id="4bce8-132">Otros recursos se mantienen en la memoria de la CPU, independientemente del dispositivo que se use.</span><span class="sxs-lookup"><span data-stu-id="4bce8-132">Other resources are kept in CPU memory, regardless of what device is used.</span></span> <span data-ttu-id="4bce8-133">Estos recursos son *independientes del dispositivo*, ya que no están asociados a un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="4bce8-133">These resources are *device-independent*, because they are not associated with a particular device.</span></span> <span data-ttu-id="4bce8-134">No es necesario volver a crear recursos independientes del dispositivo cuando cambia el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bce8-134">It is not necessary to re-create device-independent resources when the device changes.</span></span> <span data-ttu-id="4bce8-135">Los estilos y las geometrías de trazo son recursos independientes del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bce8-135">Stroke styles and geometries are device-independent resources.</span></span>

<span data-ttu-id="4bce8-136">La documentación de MSDN para cada recurso indica si el recurso es dependiente del dispositivo o independiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bce8-136">The MSDN documentation for each resource states whether the resource is device-dependent or device-independent.</span></span> <span data-ttu-id="4bce8-137">Cada tipo de recurso se representa mediante una interfaz que se deriva de [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span><span class="sxs-lookup"><span data-stu-id="4bce8-137">Every resource type is represented by an interface that derives from [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span></span> <span data-ttu-id="4bce8-138">Por ejemplo, los pinceles se representan mediante la interfaz [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) .</span><span class="sxs-lookup"><span data-stu-id="4bce8-138">For example, brushes are represented by the [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) interface.</span></span>

## <a name="the-direct2d-factory-object"></a><span data-ttu-id="4bce8-139">Objeto de generador de Direct2D</span><span class="sxs-lookup"><span data-stu-id="4bce8-139">The Direct2D Factory Object</span></span>

<span data-ttu-id="4bce8-140">El primer paso al usar Direct2D es crear una instancia del objeto de fábrica de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4bce8-140">The first step when using Direct2D is to create an instance of the Direct2D factory object.</span></span> <span data-ttu-id="4bce8-141">En la programación de equipos, un *generador* es un objeto que crea otros objetos.</span><span class="sxs-lookup"><span data-stu-id="4bce8-141">In computer programming, a *factory* is an object that creates other objects.</span></span> <span data-ttu-id="4bce8-142">El generador de Direct2D crea los siguientes tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="4bce8-142">The Direct2D factory creates the following types of objects:</span></span>

-   <span data-ttu-id="4bce8-143">Destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="4bce8-143">Render targets.</span></span>
-   <span data-ttu-id="4bce8-144">Recursos independientes del dispositivo, como los estilos de trazo y las geometrías.</span><span class="sxs-lookup"><span data-stu-id="4bce8-144">Device-independent resources, such as stroke styles and geometries.</span></span>

<span data-ttu-id="4bce8-145">Los recursos dependientes del dispositivo, como los pinceles y los mapas de bits, se crean mediante el objeto de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4bce8-145">Device-dependent resources, such as brushes and bitmaps, are created by the render target object.</span></span>

![diagrama que muestra el generador de direct2d.](images/graphics10.png)

<span data-ttu-id="4bce8-147">Para crear el objeto de generador de Direct2D, llame a la función [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .</span><span class="sxs-lookup"><span data-stu-id="4bce8-147">To create the Direct2D factory object, call the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



<span data-ttu-id="4bce8-148">El primer parámetro es una marca que especifica las opciones de creación.</span><span class="sxs-lookup"><span data-stu-id="4bce8-148">The first parameter is a flag that specifies creation options.</span></span> <span data-ttu-id="4bce8-149">La marca de **\_ \_ \_ un solo \_ subproceso de tipo de generador D2D1** significa que no se llamará a Direct2D desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4bce8-149">The **D2D1\_FACTORY\_TYPE\_SINGLE\_THREADED** flag means that you will not call Direct2D from multiple threads.</span></span> <span data-ttu-id="4bce8-150">Para admitir llamadas de varios subprocesos, especifique el tipo de generador de D2D1 de varios **\_ \_ \_ \_ subprocesos**.</span><span class="sxs-lookup"><span data-stu-id="4bce8-150">To support calls from multiple threads, specify **D2D1\_FACTORY\_TYPE\_MULTI\_THREADED**.</span></span> <span data-ttu-id="4bce8-151">Si el programa usa un solo subproceso para llamar a Direct2D, la opción de un solo subproceso es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="4bce8-151">If your program uses a single thread to call into Direct2D, the single-threaded option is more efficient.</span></span>

<span data-ttu-id="4bce8-152">El segundo parámetro de la función [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) recibe un puntero a la interfaz [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="4bce8-152">The second parameter to the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function receives a pointer to the [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) interface.</span></span>

<span data-ttu-id="4bce8-153">Debe crear el objeto de fábrica de Direct2D antes del primer mensaje de [**\_ dibujo de WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="4bce8-153">You should create the Direct2D factory object before the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="4bce8-154">El controlador de [**\_ creación**](/windows/desktop/winmsg/wm-create) de mensajes de WM es un buen lugar para crear el generador:</span><span class="sxs-lookup"><span data-stu-id="4bce8-154">The [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message handler is a good place to create the factory:</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a><span data-ttu-id="4bce8-155">Crear recursos de Direct2D</span><span class="sxs-lookup"><span data-stu-id="4bce8-155">Creating Direct2D Resources</span></span>

<span data-ttu-id="4bce8-156">El programa círculo usa los siguientes recursos dependientes del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="4bce8-156">The Circle program uses the following device-dependent resources:</span></span>

-   <span data-ttu-id="4bce8-157">Destino de representación que está asociado a la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4bce8-157">A render target that is associated with the application window.</span></span>
-   <span data-ttu-id="4bce8-158">Pincel de color sólido para pintar el círculo.</span><span class="sxs-lookup"><span data-stu-id="4bce8-158">A solid-color brush to paint the circle.</span></span>

<span data-ttu-id="4bce8-159">Cada uno de estos recursos se representa mediante una interfaz COM:</span><span class="sxs-lookup"><span data-stu-id="4bce8-159">Each of these resources is represented by a COM interface:</span></span>

-   <span data-ttu-id="4bce8-160">La interfaz [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) representa el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4bce8-160">The [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) interface represents the render target.</span></span>
-   <span data-ttu-id="4bce8-161">La interfaz [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) representa el pincel.</span><span class="sxs-lookup"><span data-stu-id="4bce8-161">The [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interface represents the brush.</span></span>

<span data-ttu-id="4bce8-162">El programa de círculo almacena punteros a estas interfaces como variables de miembro de la `MainWindow` clase:</span><span class="sxs-lookup"><span data-stu-id="4bce8-162">The Circle program stores pointers to these interfaces as member variables of the `MainWindow` class:</span></span>


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



<span data-ttu-id="4bce8-163">En el código siguiente se crean estos dos recursos.</span><span class="sxs-lookup"><span data-stu-id="4bce8-163">The following code creates these two resources.</span></span>


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



<span data-ttu-id="4bce8-164">Para crear un destino de representación para una ventana, llame al método [**ID2D1Factory:: CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) en el generador de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4bce8-164">To create a render target for a window, call the [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method on the Direct2D factory.</span></span>

-   <span data-ttu-id="4bce8-165">El primer parámetro especifica las opciones que son comunes a cualquier tipo de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4bce8-165">The first parameter specifies options that are common to any type of render target.</span></span> <span data-ttu-id="4bce8-166">Aquí, pasamos las opciones predeterminadas llamando a la función auxiliar [**D2D1:: RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span><span class="sxs-lookup"><span data-stu-id="4bce8-166">Here, we pass in default options by calling the helper function [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span></span>
-   <span data-ttu-id="4bce8-167">El segundo parámetro especifica el identificador de la ventana más el tamaño del destino de representación, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4bce8-167">The second parameter specifies the handle to the window plus the size of the render target, in pixels.</span></span>
-   <span data-ttu-id="4bce8-168">El tercer parámetro recibe un puntero [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="4bce8-168">The third parameter receives an [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pointer.</span></span>

<span data-ttu-id="4bce8-169">Para crear el pincel de color sólido, llame al método [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) en el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="4bce8-169">To create the solid-color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method on the render target.</span></span> <span data-ttu-id="4bce8-170">El color se proporciona como un [**valor \_ \_ F de color D2D1**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="4bce8-170">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) value.</span></span> <span data-ttu-id="4bce8-171">Para obtener más información sobre los colores en Direct2D, vea [usar el color en direct2d](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="4bce8-171">For more information about colors in Direct2D, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>

<span data-ttu-id="4bce8-172">Además, tenga en cuenta que si el destino de representación ya existe, el `CreateGraphicsResources` método devuelve **S \_ correcto** sin hacer nada.</span><span class="sxs-lookup"><span data-stu-id="4bce8-172">Also, notice that if the render target already exists, the `CreateGraphicsResources` method returns **S\_OK** without doing anything.</span></span> <span data-ttu-id="4bce8-173">El motivo de este diseño quedará claro en el siguiente tema.</span><span class="sxs-lookup"><span data-stu-id="4bce8-173">The reason for this design will become clear in the next topic.</span></span>

## <a name="next"></a><span data-ttu-id="4bce8-174">Siguientes</span><span class="sxs-lookup"><span data-stu-id="4bce8-174">Next</span></span>

[<span data-ttu-id="4bce8-175">Dibujo con Direct2D</span><span class="sxs-lookup"><span data-stu-id="4bce8-175">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)

 

 