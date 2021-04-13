---
title: Cómo aplicar transformaciones 2D
description: En este tema se muestra cómo aplicar transformaciones 2D a un visual mediante Microsoft DirectComposition.
ms.assetid: DED74416-C85A-4220-89BD-3F9BEF786B7D
keywords:
- Cómo aplicar transformaciones bidimensionales de DirectComposition
- Transformaciones bidimensionales de DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52d2e0ce9fbb56547c42ea4ea18d57d173a7e40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421208"
---
# <a name="how-to-apply-2d-transforms"></a><span data-ttu-id="e127c-105">Cómo aplicar transformaciones 2D</span><span class="sxs-lookup"><span data-stu-id="e127c-105">How to apply 2D transforms</span></span>

> [!NOTE]
> <span data-ttu-id="e127c-106">En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="e127c-106">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="e127c-107">Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="e127c-107">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="e127c-108">En este tema se muestra cómo aplicar transformaciones 2D a un visual mediante Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="e127c-108">This topic demonstrates how to apply 2D transforms to a visual by using Microsoft DirectComposition.</span></span> <span data-ttu-id="e127c-109">En el ejemplo de este tema se aplica un grupo de transformaciones que:</span><span class="sxs-lookup"><span data-stu-id="e127c-109">The example in this topic applies a group of transforms that:</span></span>

1.  <span data-ttu-id="e127c-110">Rote el visual en 180 grados.</span><span class="sxs-lookup"><span data-stu-id="e127c-110">Rotate the visual by 180 degrees.</span></span>
2.  <span data-ttu-id="e127c-111">Escale verticalmente el visual hasta tres veces su tamaño original.</span><span class="sxs-lookup"><span data-stu-id="e127c-111">Scale up the visual to three times its original size.</span></span>
3.  <span data-ttu-id="e127c-112">Traduzca (mueva) el visual 150 píxeles a la derecha de su posición original.</span><span class="sxs-lookup"><span data-stu-id="e127c-112">Translate (move) the visual 150 pixels to the right of its original position.</span></span>

<span data-ttu-id="e127c-113">Las capturas de pantalla siguientes muestran el visual antes y después de aplicar las transformaciones 2D.</span><span class="sxs-lookup"><span data-stu-id="e127c-113">The following screen shots show the visual before and after applying the 2D transforms.</span></span>

![resultado de aplicar un grupo de transformaciones 2D a un visual](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="e127c-115">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="e127c-115">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e127c-116">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="e127c-116">Technologies</span></span>

-   [<span data-ttu-id="e127c-117">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="e127c-117">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="e127c-118">Gráficos de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e127c-118">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="e127c-119">Infraestructura de gráficos de DirectX (DXGI)</span><span class="sxs-lookup"><span data-stu-id="e127c-119">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="e127c-120">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e127c-120">Prerequisites</span></span>

-   <span data-ttu-id="e127c-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="e127c-121">C/C++</span></span>
-   <span data-ttu-id="e127c-122">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="e127c-122">Microsoft Win32</span></span>
-   <span data-ttu-id="e127c-123">Modelo de objetos componentes (COM)</span><span class="sxs-lookup"><span data-stu-id="e127c-123">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="e127c-124">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="e127c-124">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="e127c-125">Paso 1: inicializar objetos DirectComposition</span><span class="sxs-lookup"><span data-stu-id="e127c-125">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="e127c-126">Cree el objeto de dispositivo y el objeto de destino de composición.</span><span class="sxs-lookup"><span data-stu-id="e127c-126">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="e127c-127">Cree un visual, establezca su contenido y agréguelo al árbol visual.</span><span class="sxs-lookup"><span data-stu-id="e127c-127">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="e127c-128">Para obtener más información, vea [cómo inicializar DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="e127c-128">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-transform-group-array"></a><span data-ttu-id="e127c-129">Paso 2: crear la matriz de grupos de transformación</span><span class="sxs-lookup"><span data-stu-id="e127c-129">Step 2: Create the transform group array</span></span>


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a><span data-ttu-id="e127c-130">Paso 3: crear los objetos de transformación, establecer sus propiedades y agregarlas a la matriz de grupos de transformación</span><span class="sxs-lookup"><span data-stu-id="e127c-130">Step 3: Create the transform objects, set their properties, and add them to the transform group array</span></span>

1.  <span data-ttu-id="e127c-131">Use los métodos [**IDCompositionDevice:: CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)y [**:: CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) para crear los objetos de transformación.</span><span class="sxs-lookup"><span data-stu-id="e127c-131">Use the [**IDCompositionDevice::CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform), and [**::CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) methods to create the transform objects.</span></span>
2.  <span data-ttu-id="e127c-132">Use las funciones miembro de las interfaces [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)y [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) para establecer las propiedades de las transformaciones.</span><span class="sxs-lookup"><span data-stu-id="e127c-132">Use the member functions of the [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform), and [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) interfaces to set the properties of the transforms.</span></span>
3.  <span data-ttu-id="e127c-133">Copie los punteros de la interfaz de transformación en la matriz de grupos de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="e127c-133">Copy the transform interface pointers to the transform group array.</span></span>


```C++
IDCompositionRotateTransform *pRotateTransform = nullptr;
IDCompositionScaleTransform *pScaleTransform = nullptr;
IDCompositionTranslateTransform *pTranslateTransform = nullptr;
IDCompositionTransform *pTransformGroup = nullptr;

// Create the rotate transform.
hr = pDevice->CreateRotateTransform(&pRotateTransform);

if (SUCCEEDED(hr))
{
    // Set the center of rotation to the center point of the visual.
    hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
    
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
    }

    // Set the rotate angle to 180 degrees.
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetAngle(180.0f);
    }

    // Add the rotate transform to the transform group array.
    pTransforms[0] = pRotateTransform;

    // Create the scale transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateScaleTransform(&pScaleTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Set the scaling origin to the upper-right corner of the visual.
    hr = pScaleTransform->SetCenterX(0.0f);
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetCenterY(0.0f);
    }

    // Set the scaling factor to three for both the width and height. 
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleX(3.0f);
    }
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleY(3.0f);
    }

    // Add the scale transform to the transform group array.
    pTransforms[1] = pScaleTransform;

    // Create the translate transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Move the visual 150 pixels to the right.
    hr = pTranslateTransform->SetOffsetX(150.0f);
    if (SUCCEEDED(hr)) {
        hr = pTranslateTransform->SetOffsetY(0.0f);
    }

    // Add the translate transform to the transform group array.
    pTransforms[2] = pTranslateTransform;
}
```



### <a name="step-4-create-the-transform-group-object"></a><span data-ttu-id="e127c-134">Paso 4: crear el objeto de grupo de transformación</span><span class="sxs-lookup"><span data-stu-id="e127c-134">Step 4: Create the transform group object</span></span>

<span data-ttu-id="e127c-135">Llame al método [**IDCompositionDevice:: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) para crear el objeto de grupo de transformación.</span><span class="sxs-lookup"><span data-stu-id="e127c-135">Call the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method to create the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a><span data-ttu-id="e127c-136">Paso 5: aplicar el objeto de grupo de transformación al objeto visual</span><span class="sxs-lookup"><span data-stu-id="e127c-136">Step 5: Apply the transform group object to the visual</span></span>

<span data-ttu-id="e127c-137">Use el método [**IDCompositionVisual:: SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) para asociar la propiedad transform del objeto visual con el objeto de grupo de transformación.</span><span class="sxs-lookup"><span data-stu-id="e127c-137">Use the [**IDCompositionVisual::SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) method to associate the Transform property of the visual with the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a><span data-ttu-id="e127c-138">Paso 6: confirmar la composición</span><span class="sxs-lookup"><span data-stu-id="e127c-138">Step 6: Commit the composition</span></span>

<span data-ttu-id="e127c-139">Llame al método [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para confirmar las actualizaciones del visual para DirectComposition para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="e127c-139">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the updates to the visual to DirectComposition for processing.</span></span> <span data-ttu-id="e127c-140">El resultado de aplicar el grupo de transformaciones 2D aparece en la ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="e127c-140">The result of applying the group of 2D transforms appears in the target window.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a><span data-ttu-id="e127c-141">Paso 7: liberación de los objetos DirectComposition</span><span class="sxs-lookup"><span data-stu-id="e127c-141">Step 7: Free the DirectComposition objects</span></span>

<span data-ttu-id="e127c-142">Asegúrese de liberar el grupo de objetos de transformación 2D cuando ya no los necesite.</span><span class="sxs-lookup"><span data-stu-id="e127c-142">Be sure to free the group of 2D transform objects when you no longer need them.</span></span> <span data-ttu-id="e127c-143">En el ejemplo siguiente se llama a la macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definida por la aplicación para liberar los objetos de transformación.</span><span class="sxs-lookup"><span data-stu-id="e127c-143">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the transform objects.</span></span>


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



<span data-ttu-id="e127c-144">Recuerde también que debe liberar el objeto de dispositivo, el objeto de destino de composición y los objetos visuales antes de salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e127c-144">Also remember to free the device object, the composition target object, and the visuals before your application exits.</span></span>

## <a name="complete-example"></a><span data-ttu-id="e127c-145">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="e127c-145">Complete example</span></span>


```C++
#define BITMAP_WIDTH  80.0
#define BITMAP_HEIGHT 80.0

HRESULT DemoApp::ApplyTransformGroup(IDCompositionDevice *pDevice, 
                                     IDCompositionVisual *pVisual)
{
    HRESULT hr = S_OK;

    if (pDevice == nullptr || pVisual == nullptr)
        return E_INVALIDARG; 
    
    IDCompositionTransform *pTransforms[3];

    IDCompositionRotateTransform *pRotateTransform = nullptr;
    IDCompositionScaleTransform *pScaleTransform = nullptr;
    IDCompositionTranslateTransform *pTranslateTransform = nullptr;
    IDCompositionTransform *pTransformGroup = nullptr;

    // Create the rotate transform.
    hr = pDevice->CreateRotateTransform(&pRotateTransform);

    if (SUCCEEDED(hr))
    {
        // Set the center of rotation to the center point of the visual.
        hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
        
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
        }

        // Set the rotate angle to 180 degrees.
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetAngle(180.0f);
        }

        // Add the rotate transform to the transform group array.
        pTransforms[0] = pRotateTransform;

        // Create the scale transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateScaleTransform(&pScaleTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the scaling origin to the upper-right corner of the visual.
        hr = pScaleTransform->SetCenterX(0.0f);
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetCenterY(0.0f);
        }

        // Set the scaling factor to three for both the width and height. 
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleX(3.0f);
        }
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleY(3.0f);
        }

        // Add the scale transform to the transform group array.
        pTransforms[1] = pScaleTransform;

        // Create the translate transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Move the visual 150 pixels to the right.
        hr = pTranslateTransform->SetOffsetX(150.0f);
        if (SUCCEEDED(hr)) {
            hr = pTranslateTransform->SetOffsetY(0.0f);
        }

        // Add the translate transform to the transform group array.
        pTransforms[2] = pTranslateTransform;
    }

    if (SUCCEEDED(hr))
    {
        // Create the transform group.
        hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the transform group to the visual.
        hr = pVisual->SetTransform(pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the composition.
        hr = pDevice->Commit();
    }

    // Release the transform objects.
    for (int i = 0; i < 3; i++)
    {
        SafeRelease(&pTransforms[i]);
    }

    // Release the transform group pointer.
    SafeRelease(&pTransformGroup);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="e127c-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e127c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e127c-147">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="e127c-147">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 