---
description: En este tema se describe cómo usar diferentes tipos de pinceles en un OM XPS.
ms.assetid: 392ca1d5-283e-4eed-ae21-6477c469014d
title: Pinceles de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0557757bfaf81156b2015525d35897cfb042e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687301"
---
# <a name="xps-om-brushes"></a><span data-ttu-id="a6ea0-103">Pinceles de XPS OM</span><span class="sxs-lookup"><span data-stu-id="a6ea0-103">XPS OM Brushes</span></span>

<span data-ttu-id="a6ea0-104">En este tema se describe cómo usar diferentes tipos de pinceles en un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="a6ea0-104">This topic describes how to use different types of brushes in an XPS OM.</span></span>

<span data-ttu-id="a6ea0-105">Los pinceles del OM XPS se basan en la [**interfaz IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) e incluyen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a6ea0-105">The brushes in the XPS OM are based on the [**IXpsOMBrush Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) and include the following:</span></span>

<dl> <span data-ttu-id="a6ea0-106">Pinceles de mosaico</span><span class="sxs-lookup"><span data-stu-id="a6ea0-106">Tile Brushes</span></span>

-   [<span data-ttu-id="a6ea0-107">**Interfaz IXpsOMTileBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-107">**IXpsOMTileBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
-   [<span data-ttu-id="a6ea0-108">**Interfaz IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-108">**IXpsOMSolidColorBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
-   [<span data-ttu-id="a6ea0-109">**Interfaz IXpsOMVisualBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-109">**IXpsOMVisualBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
-   [<span data-ttu-id="a6ea0-110">**Interfaz IXpsOMImageBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-110">**IXpsOMImageBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)

  
<span data-ttu-id="a6ea0-111">Pinceles de degradado</span><span class="sxs-lookup"><span data-stu-id="a6ea0-111">Gradient Brushes</span></span>

-   [<span data-ttu-id="a6ea0-112">**Interfaz IXpsOMGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-112">**IXpsOMGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
-   [<span data-ttu-id="a6ea0-113">**Interfaz IXpsOMLinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-113">**IXpsOMLinearGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
-   [<span data-ttu-id="a6ea0-114">**Interfaz IXpsOMRadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-114">**IXpsOMRadialGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)

  
</dl>

## <a name="code-examples"></a><span data-ttu-id="a6ea0-115">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="a6ea0-115">Code Examples</span></span>

### <a name="create-a-solid-color-brush"></a><span data-ttu-id="a6ea0-116">Crear un pincel de color sólido</span><span class="sxs-lookup"><span data-stu-id="a6ea0-116">Create a solid-color brush</span></span>

<span data-ttu-id="a6ea0-117">En el ejemplo de código siguiente se crea un pincel de color sólido a partir de un valor de color que se define en el código.</span><span class="sxs-lookup"><span data-stu-id="a6ea0-117">The following code example creates a solid-color brush from a color value that is defined in the code.</span></span>


```C++
    HRESULT                hr = S_OK;

    XPS_COLOR              xpsColor;
    IXpsOMSolidColorBrush  *brush;

    // creates a solid red brush
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush(
       &xpsColor, 
       NULL, 
       reinterpret_cast<IXpsOMSolidColorBrush**>(&brush));
    
    // use brush

    // when finished with brush, release pointer
    brush->Release();
```



### <a name="create-a-visual-brush"></a><span data-ttu-id="a6ea0-118">Crear un pincel visual</span><span class="sxs-lookup"><span data-stu-id="a6ea0-118">Create a visual brush</span></span>

<span data-ttu-id="a6ea0-119">En el ejemplo de código siguiente se crea un pincel a partir de un objeto visual.</span><span class="sxs-lookup"><span data-stu-id="a6ea0-119">The following code example creates a brush from a visual object.</span></span>


```C++
    HRESULT                       hr = S_OK;
    IXpsOMVisualBrush             *brush;

    XPS_RECT viewBoxRect = {0,0,0,0};
    XPS_RECT viewPortRect = {0,0,0,0};

    // set viewBoxRect to define the portion of the visual to use
    // as the brush.
    //
    // set viewPortRect to define the location and size of the 
    // the brush in the destination 
    //
    // create the brush
    hr = xpsFactory->CreateVisualBrush (
        &viewBoxRect,
        &viewPortRect,
        reinterpret_cast<IXpsOMVisualBrush**>(&brush));

    // assign the visual object
    //   brushVisual points to a visual
    //   that is defined outside of this example

    hr = brush->SetVisualLocal (brushVisual);
    
    // use brush
    
    // when finished with brush, release pointer
    brush->Release();
    
```



### <a name="create-an-image-brush"></a><span data-ttu-id="a6ea0-120">Crear un pincel de imagen</span><span class="sxs-lookup"><span data-stu-id="a6ea0-120">Create an image brush</span></span>

<span data-ttu-id="a6ea0-121">Consulte el ejemplo de código en [colocar imágenes en un OM XPS](place-images-in-an-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="a6ea0-121">Refer to the code example in [Place Images in an XPS OM](place-images-in-an-xps-om.md).</span></span>

### <a name="create-a-linear-gradient-brush"></a><span data-ttu-id="a6ea0-122">Creación de un pincel de degradado lineal</span><span class="sxs-lookup"><span data-stu-id="a6ea0-122">Create a linear-gradient brush</span></span>

<span data-ttu-id="a6ea0-123">En el ejemplo de código siguiente se crea un pincel de degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="a6ea0-123">The following code example creates a linear-gradient brush.</span></span> <span data-ttu-id="a6ea0-124">El degradado tiene dos delimitadores de degradado.</span><span class="sxs-lookup"><span data-stu-id="a6ea0-124">The gradient has two gradient stops.</span></span>


```C++
    HRESULT                       hr = S_OK;
    XPS_COLOR                     xpsColorStop;
    IXpsOMGradientStop            *xpsGradientStop1, *xpsGradientStop2;
    IXpsOMLinearGradientBrush     *brush;
    XPS_POINT                     startPoint, endPoint;

    // define the start color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xE4;
    xpsColorStop.value.sRGB.green = 0x3B;
    xpsColorStop.value.sRGB.blue  = 0x2F;
    
    // create a gradient stop by setting the color and location 
    // for the beginning of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop, 
        NULL, 
        0.0f,
        &xpsGradientStop1);
    startPoint.x = 375.75f;
    startPoint.y = 18.0f;

    // define the end color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xEF;
    xpsColorStop.value.sRGB.green = 0x79;
    xpsColorStop.value.sRGB.blue  = 0x2F;

    // create a gradient stop by setting the color and  location
    //  for the end of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop,
        NULL, 
        1.0f, 
        &xpsGradientStop2);
    endPoint.x   = 375.75f;
    endPoint.y   = 134.6f;

    // create the brush
    hr = xpsFactory->CreateLinearGradientBrush(
        xpsGradientStop1, 
        xpsGradientStop2, 
        &startPoint, 
        &endPoint, 
        &brush);
    // release gradient stops after creating brush
    xpsGradientStop1->Release();
    xpsGradientStop2->Release();

    // when finished with brush, release pointer to brush
    brush->Release();
```



## <a name="related-topics"></a><span data-ttu-id="a6ea0-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6ea0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6ea0-126">**Interfaz IXpsOMGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-126">**IXpsOMGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
</dt> <dt>

[<span data-ttu-id="a6ea0-127">**Interfaz IXpsOMImageBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-127">**IXpsOMImageBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[<span data-ttu-id="a6ea0-128">**Interfaz IXpsOMLinearGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-128">**IXpsOMLinearGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
</dt> <dt>

[<span data-ttu-id="a6ea0-129">**Interfaz IXpsOMRadialGradientBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-129">**IXpsOMRadialGradientBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)
</dt> <dt>

[<span data-ttu-id="a6ea0-130">**Interfaz IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-130">**IXpsOMSolidColorBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="a6ea0-131">**Interfaz IXpsOMTileBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-131">**IXpsOMTileBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
</dt> <dt>

[<span data-ttu-id="a6ea0-132">**Interfaz IXpsOMVisualBrush**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-132">**IXpsOMVisualBrush Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
</dt> <dt>

[<span data-ttu-id="a6ea0-133">**\_color XPS**</span><span class="sxs-lookup"><span data-stu-id="a6ea0-133">**XPS\_COLOR**</span></span>](xps-color.md)
</dt> <dt>

[<span data-ttu-id="a6ea0-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="a6ea0-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



