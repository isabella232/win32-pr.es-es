---
title: Cómo recortar con un objeto de recorte de rectángulo
description: En este tema se muestra cómo usar un objeto de clip de rectángulo para recortar un árbol visual o visual.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078582"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a><span data-ttu-id="b6a2d-103">Cómo recortar con un objeto de recorte de rectángulo</span><span class="sxs-lookup"><span data-stu-id="b6a2d-103">How to clip with a rectangle clip object</span></span>

> [!NOTE]
> <span data-ttu-id="b6a2d-104">En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="b6a2d-105">Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="b6a2d-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="b6a2d-106">En este tema se muestra cómo usar un objeto de clip de rectángulo para recortar un árbol visual o visual.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-106">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span>

<span data-ttu-id="b6a2d-107">En el ejemplo de este tema se define un clip rectangular que se centra en la ubicación del mouse y se aplica el clip a un visual que está centrado en el área cliente de la ventana de destino de la composición.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-107">The example in this topic defines a rectangular clip that is centered at the mouse location, and applies the clip to a visual that is centered in the client area of the composition target window.</span></span> <span data-ttu-id="b6a2d-108">En esta captura de pantalla se muestra el resultado de aplicar el objeto de clip de rectángulo al objeto visual.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-108">This screen shot shows the result of applying the rectangle clip object to the visual.</span></span>

![resultado de aplicar un objeto de clip de rectángulo a un objeto visual](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="b6a2d-110">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="b6a2d-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b6a2d-111">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="b6a2d-111">Technologies</span></span>

-   [<span data-ttu-id="b6a2d-112">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b6a2d-112">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="b6a2d-113">Gráficos de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b6a2d-113">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="b6a2d-114">Infraestructura de gráficos de DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="b6a2d-114">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="b6a2d-115">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6a2d-115">Prerequisites</span></span>

-   <span data-ttu-id="b6a2d-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="b6a2d-116">C/C++</span></span>
-   <span data-ttu-id="b6a2d-117">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="b6a2d-117">Microsoft Win32</span></span>
-   <span data-ttu-id="b6a2d-118">Modelo de objetos componentes (COM)</span><span class="sxs-lookup"><span data-stu-id="b6a2d-118">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="b6a2d-119">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="b6a2d-119">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="b6a2d-120">Paso 1: inicializar objetos DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b6a2d-120">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="b6a2d-121">Cree el objeto de dispositivo y el objeto de destino de composición.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-121">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="b6a2d-122">Cree un visual, establezca su contenido y agréguelo al árbol visual.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-122">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="b6a2d-123">Para obtener más información, vea [cómo inicializar DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="b6a2d-123">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-rectangle-clip-object"></a><span data-ttu-id="b6a2d-124">Paso 2: crear el objeto de clip de rectángulo</span><span class="sxs-lookup"><span data-stu-id="b6a2d-124">Step 2: Create the rectangle clip object</span></span>

<span data-ttu-id="b6a2d-125">Use el método [**IDCompositionDevice:: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) para crear una instancia del objeto de clip de rectángulo.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-125">Use the [**IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) method to create an instance of the rectangle clip object.</span></span>


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a><span data-ttu-id="b6a2d-126">Paso 3: establecer las propiedades del objeto de clip de rectángulo</span><span class="sxs-lookup"><span data-stu-id="b6a2d-126">Step 3: Set the properties of the rectangle clip object</span></span>

<span data-ttu-id="b6a2d-127">Llame a los métodos de la interfaz [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) del objeto de clip de rectángulo para establecer las propiedades del rectángulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-127">Call the methods of the rectangle clip object's [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface to set the properties of the clip rectangle.</span></span>

<span data-ttu-id="b6a2d-128">En el ejemplo siguiente se define un rectángulo de recorte que está centrado alrededor de la ubicación actual del mouse.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-128">The following example defines a clip rectangle that is centered around the current mouse location.</span></span> <span data-ttu-id="b6a2d-129">Las `m_offsetX` `m_offsetY` variables de miembro y contienen los valores de las propiedades OffsetX y OffsetY del elemento visual.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-129">The `m_offsetX` and `m_offsetY` member variables contain the values of the OffsetX and OffsetY properties of the visual.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Get the location of the mouse.
        POINT ptMouse = { };
        GetCursorPos(&ptMouse);
        ScreenToClient(m_hwnd, &ptMouse);

        // Create a 100-by-100 pixel rectangular clip that is 
        // centered at the mouse location, and is mapped to
        // the rectangle of the visual.
        m_pClip->SetLeft((ptMouse.x - m_offsetX) - 50.f);
        m_pClip->SetTop((ptMouse.y - m_offsetY) - 50.f);
        m_pClip->SetRight((ptMouse.x - m_offsetX) + 50.f);
        m_pClip->SetBottom((ptMouse.y - m_offsetY) + 50.f);
    }
```



<span data-ttu-id="b6a2d-130">Tenga en cuenta que la interfaz [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) incluye los siguientes métodos para definir un rectángulo de recorte con esquinas redondeadas:</span><span class="sxs-lookup"><span data-stu-id="b6a2d-130">Note that the [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface includes the following methods for defining a clip rectangle that has rounded corners:</span></span>

-   <span data-ttu-id="b6a2d-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="b6a2d-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span></span>
-   <span data-ttu-id="b6a2d-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="b6a2d-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span></span>
-   <span data-ttu-id="b6a2d-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="b6a2d-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span></span>
-   <span data-ttu-id="b6a2d-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="b6a2d-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span></span>

### <a name="step-4-set-the-clip-property-of-the-visual"></a><span data-ttu-id="b6a2d-135">Paso 4: establecer la propiedad clip del visual</span><span class="sxs-lookup"><span data-stu-id="b6a2d-135">Step 4: Set the Clip property of the visual</span></span>

<span data-ttu-id="b6a2d-136">Use el método [**IDCompositionVisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) para asociar la propiedad clip del objeto visual con el objeto de clip de rectángulo.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-136">Use the [**IDCompositionVisual::SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) method to associate the Clip property of the visual with the rectangle clip object.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a><span data-ttu-id="b6a2d-137">Paso 5: confirmar la composición</span><span class="sxs-lookup"><span data-stu-id="b6a2d-137">Step 5: Commit the composition</span></span>

<span data-ttu-id="b6a2d-138">Llame al método [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para confirmar el lote de comandos en Microsoft DirectComposition para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-138">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to Microsoft DirectComposition for processing.</span></span> <span data-ttu-id="b6a2d-139">El resultado de aplicar el rectángulo de recorte aparece en la ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-139">The result of applying the clip rectangle appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a><span data-ttu-id="b6a2d-140">Paso 6: liberación de los objetos DirectComposition</span><span class="sxs-lookup"><span data-stu-id="b6a2d-140">Step 6: Free the DirectComposition objects</span></span>

<span data-ttu-id="b6a2d-141">Asegúrese de liberar el objeto de clip de rectángulo cuando ya no lo necesite, así como el objeto de dispositivo, el objeto de destino de composición y los objetos visuales.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-141">Be sure to free the rectangle clip object when you no longer need it, as well as the device object, the composition target object, and any visual objects.</span></span> <span data-ttu-id="b6a2d-142">En el ejemplo siguiente se llama a la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definida por la aplicación para liberar los objetos DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="b6a2d-142">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the DirectComposition objects.</span></span>


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a><span data-ttu-id="b6a2d-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b6a2d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6a2d-144">Recorte</span><span class="sxs-lookup"><span data-stu-id="b6a2d-144">Clipping</span></span>](clipping.md)
</dt> </dl>

 

 