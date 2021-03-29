---
title: 'Información general sobre los pinceles '
description: Describe los diferentes tipos de pinceles que proporciona Direct2D.
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104421585"
---
# <a name="brushes-overview"></a><span data-ttu-id="eff97-103">Información general sobre los pinceles </span><span class="sxs-lookup"><span data-stu-id="eff97-103">Brushes overview</span></span>

<span data-ttu-id="eff97-104">En esta información general se describe cómo crear y usar los objetos [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)y [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para pintar áreas con colores sólidos, degradados y mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="eff97-104">This overview describes how to create and use [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) objects to paint areas with solid colors, gradients, and bitmaps.</span></span> <span data-ttu-id="eff97-105">Contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="eff97-105">It contains the following sections.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eff97-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eff97-106">Prerequisites</span></span>

<span data-ttu-id="eff97-107">En esta información general se supone que está familiarizado con la estructura de una aplicación básica de Direct2D, tal como se describe en [creación de una aplicación sencilla de direct2d](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="eff97-107">This overview assumes that you are familiar with the structure of a basic Direct2D application, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="brush-types"></a><span data-ttu-id="eff97-108">Tipos de pincel</span><span class="sxs-lookup"><span data-stu-id="eff97-108">Brush types</span></span>

<span data-ttu-id="eff97-109">Un pincel "pinta" un área con su salida.</span><span class="sxs-lookup"><span data-stu-id="eff97-109">A brush "paints" an area with its output.</span></span> <span data-ttu-id="eff97-110">Distintos pinceles tienen tipos de salida diferentes.</span><span class="sxs-lookup"><span data-stu-id="eff97-110">Different brushes have different types of output.</span></span> <span data-ttu-id="eff97-111">Direct2D proporciona cuatro tipos de pincel: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) pinta un área con un color sólido, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) con un degradado lineal, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) con un degradado radial y [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="eff97-111">Direct2D provides four brush types: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints an area with a solid color, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) with a linear gradient, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) with a radial gradient, and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with a bitmap.</span></span>

> [!NOTE]  
> <span data-ttu-id="eff97-112">A partir de Windows 8, también puede usar [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), que es similar a un pincel de mapa de bits, pero también puede usar primitivas.</span><span class="sxs-lookup"><span data-stu-id="eff97-112">Starting with Windows 8, you can also use [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), which is similar to a bitmap brush, but you can use primitives, too.</span></span>

<span data-ttu-id="eff97-113">Todos los pinceles se heredan de [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) y comparten un conjunto de características comunes (estableciendo y obteniendo la opacidad y transformando los pinceles); se crean mediante [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) y son recursos dependientes del dispositivo: la aplicación debe crear pinceles después de inicializar el destino de representación con el que se usarán los pinceles y volver a crear los pinceles cada vez que sea necesario volver a crear el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="eff97-113">All brushes inherit from [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) and share a set of common features (setting and getting opacity, and transforming brushes); they are created by [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) and are device-dependent resources: your application should create brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated.</span></span> <span data-ttu-id="eff97-114">(Para obtener más información acerca de los recursos, consulte [información general sobre recursos](resources-and-resource-domains.md)).</span><span class="sxs-lookup"><span data-stu-id="eff97-114">(For more information about resources, see [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="eff97-115">En la ilustración siguiente se muestran ejemplos de cada uno de los distintos tipos de pincel.</span><span class="sxs-lookup"><span data-stu-id="eff97-115">The following illustration shows examples of each of the different brush types.</span></span>

![Ilustración de los efectos visuales de los pinceles de color sólido, pinceles de degradado lineal, pinceles de degradado radial y pinceles de mapa de bits](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a><span data-ttu-id="eff97-117">Conceptos básicos de color</span><span class="sxs-lookup"><span data-stu-id="eff97-117">Color basics</span></span>

<span data-ttu-id="eff97-118">Antes de pintar con un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) o un pincel de degradado, debe elegir colores.</span><span class="sxs-lookup"><span data-stu-id="eff97-118">Before you paint with an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or a gradient brush, you need to choose colors.</span></span> <span data-ttu-id="eff97-119">En Direct2D, los colores se representan mediante la estructura de [**\_ color \_ F de D2D1**](d2d1-color-f.md) (que, en realidad, es simplemente un nombre nuevo para la estructura que usa Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span><span class="sxs-lookup"><span data-stu-id="eff97-119">In Direct2D, colors are represented by the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure (which is actually just a new name for the structure that is used by Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span></span>

<span data-ttu-id="eff97-120">Antes de Windows 8, [**el \_ color \_ F de D2D1**](d2d1-color-f.md) usa la codificación sRGB.</span><span class="sxs-lookup"><span data-stu-id="eff97-120">Prior to Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) uses sRGB encoding.</span></span> <span data-ttu-id="eff97-121">la codificación sRGB divide los colores en cuatro componentes: rojo, verde, azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="eff97-121">sRGB encoding divides colors into four components: red, green, blue, and alpha.</span></span> <span data-ttu-id="eff97-122">Cada componente se representa mediante un valor de punto flotante con un intervalo normal de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="eff97-122">Each component is represented by a floating point value with a normal range of 0.0 to 1.0.</span></span> <span data-ttu-id="eff97-123">Un valor de 0,0 indica la ausencia completa de ese color, mientras que un valor de 1,0 indica que el color está completamente presente.</span><span class="sxs-lookup"><span data-stu-id="eff97-123">A value of 0.0 indicates the complete absence of that color, while a value of 1.0 indicates that the color is fully present.</span></span> <span data-ttu-id="eff97-124">Para el componente alfa, 0,0 representa un color completamente transparente y 1,0 representa un color totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="eff97-124">For the alpha component, 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span>

<span data-ttu-id="eff97-125">A partir de Windows 8, el [**\_ color \_ F de D2D1**](d2d1-color-f.md) también acepta la codificación ScRGB.</span><span class="sxs-lookup"><span data-stu-id="eff97-125">Starting in Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) also accepts scRGB encoding.</span></span> <span data-ttu-id="eff97-126">scRGB es un superconjunto de que permite valores de color por encima de 1,0 y por debajo de 0,0.</span><span class="sxs-lookup"><span data-stu-id="eff97-126">scRGB is a superset of that allows color values above 1.0 and below 0.0.</span></span>

<span data-ttu-id="eff97-127">Para definir un color, puede usar la estructura [**D2D1 de \_ color \_ F**](d2d1-color-f.md) e inicializar sus campos usted mismo, o bien puede usar la clase [**D2D1:: ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para ayudarle a crear el color.</span><span class="sxs-lookup"><span data-stu-id="eff97-127">To define a color, you can use the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure and initialize its fields yourself, or you can use the [**D2D1::ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to help you create the color.</span></span> <span data-ttu-id="eff97-128">La clase **ColorF** proporciona varios constructores para definir colores.</span><span class="sxs-lookup"><span data-stu-id="eff97-128">The **ColorF** class provides several constructors for defining colors.</span></span> <span data-ttu-id="eff97-129">Si el valor alfa no se especifica en los constructores, se toma como valor predeterminado 1,0.</span><span class="sxs-lookup"><span data-stu-id="eff97-129">If the alpha value is not specified in the constructors, it defaults to 1.0.</span></span>

-   <span data-ttu-id="eff97-130">Use el constructor [**ColorF (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) para especificar un color predefinido y un valor de canal alfa.</span><span class="sxs-lookup"><span data-stu-id="eff97-130">Use the [**ColorF(Enum, FLOAT)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) constructor to specify a predefined color and an alpha channel value.</span></span> <span data-ttu-id="eff97-131">Un valor de canal alfa oscila entre 0,0 y 1,0, donde 0,0 representa un color completamente transparente y 1,0 representa un color totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="eff97-131">An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span> <span data-ttu-id="eff97-132">En la ilustración siguiente se muestran varios colores predefinidos y sus equivalentes hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="eff97-132">The following illustration shows several predefined colors and their hexadecimal equivalents.</span></span> <span data-ttu-id="eff97-133">Para obtener una lista completa de los colores predefinidos, vea la sección de constantes de color de la clase [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="eff97-133">For a complete list of predefined colors, see the Color constants section of the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span>

    ![Ilustración de los colores predefinidos](images/brushes-ovw-colors.png)

    <span data-ttu-id="eff97-135">En el ejemplo siguiente se crea un color predefinido y se usa para especificar el color de un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="eff97-135">The following example creates a predefined color and uses it to specify the color of an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   <span data-ttu-id="eff97-136">Use el constructor [**ColorF (float, Float, Float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) para especificar un color en la secuencia de un rojo, verde, azul y alfa, donde cada elemento tiene un valor entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="eff97-136">Use the [**ColorF(FLOAT, FLOAT, FLOAT, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) constructor to specify a color in the sequence of a red, green, blue, and alpha, where each element has a value between 0.0 and 1.0.</span></span>

    <span data-ttu-id="eff97-137">En el ejemplo siguiente se especifican los valores rojo, verde, azul y alfa de un color.</span><span class="sxs-lookup"><span data-stu-id="eff97-137">The following example specifies the red, green, blue, and alpha values for a color.</span></span>

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   <span data-ttu-id="eff97-138">Use el constructor [**ColorF (UINT32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) para especificar el valor hexadecimal de un color y un valor alfa, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="eff97-138">Use the [**ColorF(UINT32, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) constructor to specify the hexadecimal value of a color and an alpha value, as shown in the following example.</span></span>
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a><span data-ttu-id="eff97-139">Modos alfa</span><span class="sxs-lookup"><span data-stu-id="eff97-139">Alpha modes</span></span>

<span data-ttu-id="eff97-140">Independientemente del modo alfa del destino de representación con el que se usa un pincel, los valores de [**\_ color \_ F de D2D1**](d2d1-color-f.md) siempre se interpretan como alfa recto.</span><span class="sxs-lookup"><span data-stu-id="eff97-140">Regardless of the alpha mode of the render target with which you use a brush, [**D2D1\_COLOR\_F**](d2d1-color-f.md) values are always interpreted as straight alpha.</span></span>

## <a name="using-solid-color-brushes"></a><span data-ttu-id="eff97-141">Usar pinceles de color sólido</span><span class="sxs-lookup"><span data-stu-id="eff97-141">Using solid color brushes</span></span>

<span data-ttu-id="eff97-142">Para crear un pincel de color sólido, llame al método [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , que devuelve un valor HRESULT y un objeto [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) .</span><span class="sxs-lookup"><span data-stu-id="eff97-142">To create a solid color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method, which returns an HRESULT and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) object.</span></span> <span data-ttu-id="eff97-143">En la ilustración siguiente se muestra un cuadrado con trazos con un pincel de color negro y pintado con un pincel de color sólido que tiene el valor de color de 0x9ACD32.</span><span class="sxs-lookup"><span data-stu-id="eff97-143">The following illustration shows a square that is stroked with a black color brush and painted with a solid color brush that has the color value of 0x9ACD32.</span></span>

![Ilustración de un cuadrado pintado con un pincel de color sólido](images/brushes-ovw-solidcolor.png)

<span data-ttu-id="eff97-145">En el código siguiente se muestra cómo crear y usar un pincel de color negro y un pincel con un valor de color de 0x9ACD32 para rellenar y dibujar este cuadrado.</span><span class="sxs-lookup"><span data-stu-id="eff97-145">The following code shows how to create and use a black color brush and a brush with a color value of 0x9ACD32 to fill and draw this square.</span></span>


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



<span data-ttu-id="eff97-146">A diferencia de otros pinceles, la creación de una [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) es una operación relativamente económica.</span><span class="sxs-lookup"><span data-stu-id="eff97-146">Unlike other brushes, creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is a relatively inexpensive operation.</span></span> <span data-ttu-id="eff97-147">Puede crear objetos **ID2D1SolidColorBrush** cada vez que represente con poco o ningún impacto en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="eff97-147">You may create **ID2D1SolidColorBrush** objects each time you render with little to no performance impact.</span></span> <span data-ttu-id="eff97-148">Este enfoque no se recomienda para los pinceles de degradado o de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="eff97-148">This approach is not recommended for gradient or bitmap brushes.</span></span>

## <a name="using-linear-gradient-brushes"></a><span data-ttu-id="eff97-149">Usar pinceles de degradado lineal</span><span class="sxs-lookup"><span data-stu-id="eff97-149">Using linear gradient brushes</span></span>

<span data-ttu-id="eff97-150">Un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) pinta un área con un degradado lineal definido a lo largo de una línea, el eje de degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-150">An [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) paints an area with a linear gradient defined along a line, the gradient axis.</span></span> <span data-ttu-id="eff97-151">Los colores del degradado y su ubicación se especifican a lo largo del eje de degradado mediante objetos [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) .</span><span class="sxs-lookup"><span data-stu-id="eff97-151">You specify the gradient's colors and their location along the gradient axis using [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) objects.</span></span> <span data-ttu-id="eff97-152">También puede modificar el eje de degradado, que le permite crear un degradado horizontal y vertical, e invertir la dirección del degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-152">You may also modify the gradient axis, which enables you to create horizontal and vertical gradient and to reverse the gradient direction.</span></span> <span data-ttu-id="eff97-153">Para crear un pincel de degradado lineal, llame al método [**ID2D1RenderTarget:: CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .</span><span class="sxs-lookup"><span data-stu-id="eff97-153">To create a linear gradient brush, call the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method.</span></span>

<span data-ttu-id="eff97-154">En la ilustración siguiente se muestra un cuadrado que se pinta con un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) que tiene dos colores predefinidos: "Yellow" y "ForestGreen".</span><span class="sxs-lookup"><span data-stu-id="eff97-154">The following illustration shows a square that is painted with an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that has two predefined colors, "Yellow" and "ForestGreen".</span></span>

![Ilustración de un cuadrado pintado con un pincel de degradado lineal de amarillo y verde de bosque](images/brushes-ovw-lineargradient.png)

<span data-ttu-id="eff97-156">Para crear el degradado que se muestra en la ilustración anterior, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="eff97-156">To create the gradient shown in the preceding illustration, complete these steps:</span></span>

1.  <span data-ttu-id="eff97-157">Declare dos objetos de delimitador de [**\_ \_ degradado D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="eff97-157">Declare two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="eff97-158">Cada delimitador de degradado especifica un color y una posición.</span><span class="sxs-lookup"><span data-stu-id="eff97-158">Each gradient stop specifies a color and a position.</span></span> <span data-ttu-id="eff97-159">Una posición de 0,0 indica el principio del degradado, mientras que una posición de 1,0 indica el final del degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-159">A position of 0.0 indicates the beginning of the gradient, while a position of 1.0 indicates the end of the gradient.</span></span>

    <span data-ttu-id="eff97-160">En el código siguiente se crea una matriz de dos objetos de delimitador de [**\_ \_ degradado D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="eff97-160">The following code creates an array of two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="eff97-161">La primera parada especifica el color "Yellow" en la posición 0 y el segundo valor de STOP especifica el color "ForestGreen" en la posición 1.</span><span class="sxs-lookup"><span data-stu-id="eff97-161">The first stop specifies the color "Yellow" at a position 0, and the second stop specifies the color "ForestGreen" at position 1.</span></span>

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  <span data-ttu-id="eff97-162">Cree un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="eff97-162">Create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span> <span data-ttu-id="eff97-163">En el ejemplo siguiente se llama a [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), pasando la matriz de objetos de delimitador de [**\_ degradado \_ D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , el número de delimitadores de degradado (2), [**D2D1 \_ gamma \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) para la interpolación y [**D2D1 la \_ \_ \_ abrazadera del modo Extend**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) para el modo Extend.</span><span class="sxs-lookup"><span data-stu-id="eff97-163">The following example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passing in the array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects, the number of gradient stops (2), [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) for interpolation, and [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) for the extend mode.</span></span>

```C++
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
```

    

3.  <span data-ttu-id="eff97-164">Cree el [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="eff97-164">Create the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="eff97-165">En el ejemplo siguiente se llama al método [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) y se le pasan las propiedades de pincel de degradado lineal que contienen el punto inicial en (0,0) y el punto final en (150, 150) y los delimitadores de degradado creados en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="eff97-165">The next example calls the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and passes it the linear gradient brush properties that contain the start point at (0, 0) and the end point at (150, 150), and the gradient stops created in the previous step.</span></span>
```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
```

    

4.  <span data-ttu-id="eff97-166">Use [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="eff97-166">Use the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="eff97-167">En el siguiente ejemplo de código se usa el pincel para relleno un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="eff97-167">The next code example uses the brush to fille a rectangle.</span></span>
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a><span data-ttu-id="eff97-168">Más información sobre los delimitadores de degradado</span><span class="sxs-lookup"><span data-stu-id="eff97-168">More about gradient stops</span></span>

<span data-ttu-id="eff97-169">El delimitador de [**\_ degradado \_ D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) es el bloque de creación básico de un pincel de degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-169">The [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) is the basic building block of a gradient brush.</span></span> <span data-ttu-id="eff97-170">Un delimitador de degradado especifica el color y la posición a lo largo del eje de degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-170">A gradient stop specifies the color and the position along the gradient axis.</span></span> <span data-ttu-id="eff97-171">El valor de la posición del degradado oscila entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="eff97-171">The value of the gradient position ranges between 0.0 and 1.0.</span></span> <span data-ttu-id="eff97-172">Cuanto más se acerque a 0,0, más próximo será el color al inicio del degradado. cuanto más se acerque a 1,0, más próximo será el color al final del degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-172">The closer it is to 0.0, the closer the color is to the start of the gradient; the closer it is to 1.0, the closer the color is to the end of the gradient.</span></span>

<span data-ttu-id="eff97-173">En la ilustración siguiente se resaltan los delimitadores de degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-173">The following illustration highlights the gradient stops.</span></span> <span data-ttu-id="eff97-174">El círculo marca la posición de los delimitadores de degradado y una línea discontinua muestra el eje de degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-174">The circle marks the position of gradient stops and a dashed line shows the gradient axis.</span></span>

![Ilustración de un pincel de degradado lineal con cuatro paradas a lo largo del eje](images/4stoplineargradient.png)

<span data-ttu-id="eff97-176">El primer delimitador de degradado especifica el color amarillo en una posición de 0,0.</span><span class="sxs-lookup"><span data-stu-id="eff97-176">The first gradient stop specifies the color yellow at a position of 0.0.</span></span> <span data-ttu-id="eff97-177">El segundo delimitador de degradado especifica el color rojo en una posición de 0,25.</span><span class="sxs-lookup"><span data-stu-id="eff97-177">The second gradient stop specifies red color at a position of 0.25.</span></span> <span data-ttu-id="eff97-178">De izquierda a derecha a lo largo del eje de degradado, los colores entre estos dos se detienen gradualmente de amarillo a rojo.</span><span class="sxs-lookup"><span data-stu-id="eff97-178">From left to right along the gradient axis, the colors between these two stops gradually change from yellow to red.</span></span> <span data-ttu-id="eff97-179">El tercer delimitador de degradado especifica el color azul en una posición de 0,75.</span><span class="sxs-lookup"><span data-stu-id="eff97-179">The third gradient stop specifies blue color at a position of 0.75.</span></span> <span data-ttu-id="eff97-180">Los colores entre el segundo y el tercer delimitador de degradado cambian gradualmente de rojo a azul.</span><span class="sxs-lookup"><span data-stu-id="eff97-180">The colors between the second and third gradient stops gradually change from red to blue.</span></span> <span data-ttu-id="eff97-181">El cuarto delimitador de degradado especifica verde lima en una posición de 1,0.</span><span class="sxs-lookup"><span data-stu-id="eff97-181">The fourth gradient stop specifies lime green at a position of 1.0.</span></span> <span data-ttu-id="eff97-182">Los colores entre el tercer y cuarto delimitador de degradado cambian gradualmente de azul a verde lima.</span><span class="sxs-lookup"><span data-stu-id="eff97-182">The colors between the third and fourth gradient stops gradually change from blue to lime green.</span></span>

## <a name="the-gradient-axis"></a><span data-ttu-id="eff97-183">El eje de degradado</span><span class="sxs-lookup"><span data-stu-id="eff97-183">The gradient axis</span></span>

<span data-ttu-id="eff97-184">Como se mencionó anteriormente, los puntos de degradado de un pincel de degradado lineal se colocan a lo largo de una línea, el eje de degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-184">As mentioned previously, gradient stops of a linear gradient brush are positioned along a line, the gradient axis.</span></span> <span data-ttu-id="eff97-185">Puede especificar la orientación y el tamaño de la línea mediante los campos **startPoint** y **endPoint** de la estructura [**D2D1 \_ linear \_ gradiente \_ Brush \_ Properties**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) al crear un pincel de degradado lineal.</span><span class="sxs-lookup"><span data-stu-id="eff97-185">You can specify the orientation and size of the line using the **startPoint** and **endPoint** fields of the [**D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) structure when you create a linear gradient brush.</span></span> <span data-ttu-id="eff97-186">Después de crear un pincel, puede ajustar el eje de degradado llamando a los métodos [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) y [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) del pincel.</span><span class="sxs-lookup"><span data-stu-id="eff97-186">After you've created a brush, you can adjust the gradient axis by calling the brush's [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) and [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) methods.</span></span> <span data-ttu-id="eff97-187">Manipulando el punto inicial y el punto final del pincel, puede crear degradados horizontales y verticales, invertir la dirección del degradado, etc.</span><span class="sxs-lookup"><span data-stu-id="eff97-187">By manipulating the brush's start point and end point, you can create horizontal and vertical gradients, reverse the gradient direction, and more.</span></span>

<span data-ttu-id="eff97-188">Por ejemplo, en la siguiente ilustración, el punto inicial se establece en (0, 0) y el punto final en (150, 50); Esto crea un degradado diagonal que comienza en la esquina superior izquierda y se extiende a la esquina inferior derecha del área que se está pintando.</span><span class="sxs-lookup"><span data-stu-id="eff97-188">For example, in the following illustration, the start point is set to (0,0) and the end point to (150, 50); this creates a diagonal gradient that starts at the upper-left corner and extends to the lower-right corner of the area being painted.</span></span> <span data-ttu-id="eff97-189">Al establecer el punto inicial en (0, 25) y el punto final en (150, 25), se crea un degradado horizontal.</span><span class="sxs-lookup"><span data-stu-id="eff97-189">When you set the start point to (0, 25) and the end point to (150, 25), a horizontal gradient is created.</span></span> <span data-ttu-id="eff97-190">Del mismo modo, si se establece el punto inicial en (75, 0) y el punto final en (75, 50), se crea un degradado vertical.</span><span class="sxs-lookup"><span data-stu-id="eff97-190">Similarly, setting the start point to (75, 0) and the end point to (75, 50) creates a vertical gradient.</span></span> <span data-ttu-id="eff97-191">Al establecer el punto inicial en (0, 50) y el punto final en (150, 0), se crea un degradado diagonal que comienza en la esquina inferior izquierda y se extiende hasta la esquina superior derecha del área que se está pintando.</span><span class="sxs-lookup"><span data-stu-id="eff97-191">Setting the start point to (0, 50) and the end point to (150, 0) creates a diagonal gradient that starts at the lower-left corner and extends to the upper-right corner of the area being painted.</span></span>

![Ilustración de cuatro ejes de degradado diferentes en el mismo rectángulo](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a><span data-ttu-id="eff97-193">Usar pinceles de degradado radial</span><span class="sxs-lookup"><span data-stu-id="eff97-193">Using radial gradient brushes</span></span>

<span data-ttu-id="eff97-194">A diferencia de un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), que combina dos o más colores a lo largo de un eje de degradado, una [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) pinta un área con un degradado radial que combina dos o más colores a través de una elipse.</span><span class="sxs-lookup"><span data-stu-id="eff97-194">Unlike an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), which blends two or more colors along a gradient axis, an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) paints an area with a radial gradient that blends two or more colors across an ellipse.</span></span> <span data-ttu-id="eff97-195">Mientras que un **ID2D1LinearGradientBrush** define su eje de degradado con un punto inicial y un punto final, un **ID2D1RadialGradientBrush** define su elipse de degradado especificando un centro, radios horizontales y verticales, y un desplazamiento de origen del degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-195">While a **ID2D1LinearGradientBrush** defines its gradient axis with a start point and an end point, a **ID2D1RadialGradientBrush** defines its gradient ellipse by specifying a center, horizontal and vertical radii, and a gradient origin offset.</span></span>

<span data-ttu-id="eff97-196">Al igual que un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) usa un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) para especificar los colores y las posiciones del degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-196">Like an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) uses an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to specify the colors and positions in the gradient.</span></span>

<span data-ttu-id="eff97-197">En la ilustración siguiente se muestra un círculo pintado con un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="eff97-197">The following illustration shows a circle painted with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span> <span data-ttu-id="eff97-198">El círculo tiene dos delimitadores de degradado: el primero especifica un color predefinido "Yellow" en la posición 0,0 y el segundo especifica un color predefinido "ForestGreen" en una posición de 1,0.</span><span class="sxs-lookup"><span data-stu-id="eff97-198">The circle has two gradient stops: the first specifies a predefined color "Yellow" at a position of 0.0, and the second specifies a predefined color "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="eff97-199">El degradado tiene un centro de (75, 75), un desplazamiento de origen del degradado de (0,0) y un radio x e y de 75.</span><span class="sxs-lookup"><span data-stu-id="eff97-199">The gradient has a center of (75, 75), a gradient origin offset of (0, 0), and an x- and y-radius of 75.</span></span>

![Ilustración de un círculo pintado con un pincel de degradado radial](images/brushes-ovw-radials.png)

<span data-ttu-id="eff97-201">En los siguientes ejemplos de código se muestra cómo pintar este círculo con un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) que tiene dos delimitadores de color: "Yellow" en la posición 0,0 y "ForestGreen" en una posición de 1,0.</span><span class="sxs-lookup"><span data-stu-id="eff97-201">The following code examples shows how to paint this circle with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that has two color stops: "Yellow" at a position of 0.0, and "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="eff97-202">De forma similar a la creación de un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), en el ejemplo se llama a [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para crear un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) a partir de una matriz de delimitadores de degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-202">Similar to creating an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), the example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from an array of gradient stops.</span></span>


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



<span data-ttu-id="eff97-203">Para crear un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use el método [**ID2D1RenderTarget:: CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="eff97-203">To create an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use the [**ID2D1RenderTarget::CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) method.</span></span> <span data-ttu-id="eff97-204">**CreateRadialGradientBrush** toma tres parámetros.</span><span class="sxs-lookup"><span data-stu-id="eff97-204">The **CreateRadialGradientBrush** takes three parameters.</span></span> <span data-ttu-id="eff97-205">El primer parámetro, una [**\_ propiedad de \_ \_ pincel de \_ degradado radial D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) especifica el centro, el desplazamiento del origen del degradado y los radios horizontal y vertical del degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-205">The first parameter, a [**D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) specifies the center, gradient origin offset, and the horizontal and vertical radii of the gradient.</span></span> <span data-ttu-id="eff97-206">El segundo parámetro es un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) que describe los colores y sus posiciones en el degradado, y el tercer parámetro es la dirección del puntero que recibe la nueva referencia de **ID2D1RadialGradientBrush** .</span><span class="sxs-lookup"><span data-stu-id="eff97-206">The second parameter is an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) that describes the colors and their positions in the gradient, and the third parameter is the address of the pointer that receive the new **ID2D1RadialGradientBrush** reference.</span></span> <span data-ttu-id="eff97-207">Algunas sobrecargas toman un parámetro adicional, una estructura de [**\_ \_ propiedades de pincel D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) que especifica un valor de opacidad y una transformación que se va a aplicar al nuevo pincel.</span><span class="sxs-lookup"><span data-stu-id="eff97-207">Some overloads take an additional parameter, a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) structure that specifies an opacity value and a transform to apply to the new brush.</span></span>

<span data-ttu-id="eff97-208">En el ejemplo siguiente se llama a [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), se pasa la matriz de delimitadores de degradado y las propiedades de pincel de degradado radial que tienen el valor *central* establecido en (75, 75), el *gradientOriginOffset* establecido en (0,0) y *radiusX* y *RADIUS* , ambos establecidos en 75.</span><span class="sxs-lookup"><span data-stu-id="eff97-208">The next example calls [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passing in the array of gradient stops, and the radial gradient brush properties that have the *center* value set to (75, 75), the *gradientOriginOffset* set to (0, 0), and *radiusX* and *radiusY* both set to 75.</span></span>


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



<span data-ttu-id="eff97-209">En el último ejemplo se usa el pincel para rellenar una elipse.</span><span class="sxs-lookup"><span data-stu-id="eff97-209">The final example uses the brush to fill an ellipse.</span></span>


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a><span data-ttu-id="eff97-210">Configuración de un degradado radial</span><span class="sxs-lookup"><span data-stu-id="eff97-210">Configuring a radial gradient</span></span>

<span data-ttu-id="eff97-211">Los distintos valores de *Center*, *gradientOriginOffset*, *radiusX* y/o *RADIUS* generan degradados diferentes.</span><span class="sxs-lookup"><span data-stu-id="eff97-211">Different values for *center*, *gradientOriginOffset*, *radiusX* and/or *radiusY* produce different gradients.</span></span> <span data-ttu-id="eff97-212">En la ilustración siguiente se muestran varios degradados radiales con distintos desplazamientos de origen de degradado, lo que crea la apariencia de la luz que ilumina los círculos de distintos ángulos.</span><span class="sxs-lookup"><span data-stu-id="eff97-212">The following illustration shows several radial gradients that have different gradient origin offsets, creating the appearance of the light illuminating the circles from different angles.</span></span>

![Ilustración del mismo círculo pintado con pinceles de degradado radial con desplazamientos de origen diferentes](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a><span data-ttu-id="eff97-214">Usar pinceles de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="eff97-214">Using bitmap brushes</span></span>

<span data-ttu-id="eff97-215">Un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) pinta un área con un mapa de bits (representado por un objeto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).</span><span class="sxs-lookup"><span data-stu-id="eff97-215">An [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) paints an area with a bitmap (represented by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object).</span></span>

<span data-ttu-id="eff97-216">En la ilustración siguiente se muestra un cuadrado pintado con un mapa de bits de una planta.</span><span class="sxs-lookup"><span data-stu-id="eff97-216">The following illustration shows a square painted with a bitmap of a plant.</span></span>

![Ilustración de un cuadrado pintado con un mapa de bits de planta](images/brushes-ovw-bitmap.png)

<span data-ttu-id="eff97-218">En los ejemplos siguientes se muestra cómo pintar este cuadrado con un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="eff97-218">The examples that follow shows how to paint this square with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>

<span data-ttu-id="eff97-219">En el primer ejemplo se inicializa un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) para su uso con el pincel.</span><span class="sxs-lookup"><span data-stu-id="eff97-219">The first example initializes an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) for use with the brush.</span></span> <span data-ttu-id="eff97-220">El **ID2D1Bitmap** se proporciona mediante un método auxiliar, LoadResourceBitmap, que se define en otra parte del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="eff97-220">The **ID2D1Bitmap** is provided by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



<span data-ttu-id="eff97-221">Para crear el pincel de mapa de bits, llame al método [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) y especifique el [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) con el que desea pintar.</span><span class="sxs-lookup"><span data-stu-id="eff97-221">To create the bitmap brush, call the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with which to paint.</span></span> <span data-ttu-id="eff97-222">El método devuelve un **valor HRESULT** y un objeto [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) .</span><span class="sxs-lookup"><span data-stu-id="eff97-222">The method returns an **HRESULT** and an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) object.</span></span> <span data-ttu-id="eff97-223">Algunas sobrecargas de **CreateBitmapBrush** permiten especificar opciones adicionales mediante la aceptación de [**\_ \_ las propiedades de pincel de D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) y una estructura de [**\_ \_ \_ propiedades de pincel de mapa de bits de D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .</span><span class="sxs-lookup"><span data-stu-id="eff97-223">Some **CreateBitmapBrush** overloads enable you to specify additional options by accepting a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) and a [**D2D1\_BITMAP\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) structure.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



<span data-ttu-id="eff97-224">En el ejemplo siguiente se usa el pincel para rellenar un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="eff97-224">The next example uses the brush to fill a rectangle.</span></span>


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a><span data-ttu-id="eff97-225">Configurar modos de extensión</span><span class="sxs-lookup"><span data-stu-id="eff97-225">Configuring extend modes</span></span>

<span data-ttu-id="eff97-226">A veces, el degradado de un pincel de degradado o el mapa de bits para un pincel de mapa de bits no rellena completamente el área que se está pintando.</span><span class="sxs-lookup"><span data-stu-id="eff97-226">Sometimes, the gradient of a gradient brush or the bitmap for a bitmap brush doesn't completely fill the area being painted.</span></span>

-   <span data-ttu-id="eff97-227">Cuando esto sucede en un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D usa la configuración de modo de extensión horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) y vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) del pincel para determinar cómo rellenar el área restante.</span><span class="sxs-lookup"><span data-stu-id="eff97-227">When this happens for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D uses the brush's horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) and vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) extend mode settings to determine how to fill the remaining area.</span></span>

-   <span data-ttu-id="eff97-228">Cuando esto sucede en un pincel de degradado, Direct2D determina cómo rellenar el área restante mediante el valor del parámetro de [**\_ \_ modo de extensión D2D1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) que especificó al llamar a [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) para crear el [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)del pincel de degradado.</span><span class="sxs-lookup"><span data-stu-id="eff97-228">When this happens for a gradient brush, Direct2D determines how to fill the remaining area by using the value of the [**D2D1\_EXTEND\_MODE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) parameter that you specified when you called the [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create the gradient brush's [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>

<span data-ttu-id="eff97-229">En la ilustración siguiente se muestran los resultados de cada combinación posible de los modos de extensión para [**una \_ \_ \_ abrazadera en modo de extensión**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) de [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): D2D1 (clamp), **D2D1 \_ Extend \_ Mode \_ Wrap** (Wrap) y **D2D1 \_ Extend \_ Mirror** (Mirror).</span><span class="sxs-lookup"><span data-stu-id="eff97-229">The following illustration shows the results from every possible combination of the extend modes for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (CLAMP), **D2D1\_EXTEND\_MODE\_WRAP** (WRAP), and **D2D1\_EXTEND\_MIRROR** (MIRROR).</span></span>

![Ilustración de una imagen original y las imágenes resultantes de varios modos de extensión](images/bitmapwrap-clamp-mirror.png)

<span data-ttu-id="eff97-231">En el ejemplo siguiente se muestra cómo establecer los modos x-e y-Extend del pincel de mapa de bits en [**D2D1 \_ extender \_ Mirror**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="eff97-231">The following example shows how to set the bitmap brush's x- and y-extend modes to [**D2D1\_EXTEND\_MIRROR**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span> <span data-ttu-id="eff97-232">A continuación, pinta el rectángulo con el [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="eff97-232">It then paints the rectangle with the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



<span data-ttu-id="eff97-233">Genera la salida como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="eff97-233">It produces output as shown in the following illustration.</span></span>

![Ilustración de una imagen original y la imagen resultante después de reflejar las direcciones x e y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a><span data-ttu-id="eff97-235">Transformación de pinceles</span><span class="sxs-lookup"><span data-stu-id="eff97-235">Transforming brushes</span></span>

<span data-ttu-id="eff97-236">Cuando se pinta con un pincel, pinta en el espacio de coordenadas del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="eff97-236">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="eff97-237">Los pinceles no se colocan automáticamente para alinearse con el objeto que se está dibujando; de forma predeterminada, empiezan a pintar en el origen (0,0) del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="eff97-237">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="eff97-238">Puede "desplace" el degradado definido por un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) a un área de destino estableciendo el punto inicial y el punto final.</span><span class="sxs-lookup"><span data-stu-id="eff97-238">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="eff97-239">Del mismo modo, puede trasladar el degradado definido por un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) cambiando su centro y radios.</span><span class="sxs-lookup"><span data-stu-id="eff97-239">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="eff97-240">Para alinear el contenido de un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con el área que se está dibujando, puede usar el método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) para traducir el mapa de bits a la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="eff97-240">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="eff97-241">Esta transformación solo afecta al pincel; no afecta a ningún otro contenido dibujado por el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="eff97-241">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="eff97-242">En las ilustraciones siguientes se muestra el efecto de usar un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) para rellenar un rectángulo ubicado en (100, 100).</span><span class="sxs-lookup"><span data-stu-id="eff97-242">The following illustrations shows the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="eff97-243">En la ilustración de la ilustración izquierda se muestra el resultado de llenar el rectángulo sin transformar el pincel: el mapa de bits se dibuja en el origen del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="eff97-243">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="eff97-244">Como resultado, solo aparece una parte del mapa de bits en el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="eff97-244">As a result, only a portion of the bitmap appears in the rectangle.</span></span> <span data-ttu-id="eff97-245">En la ilustración de la derecha se muestra el resultado de transformar el **ID2D1BitmapBrush** para que su contenido se desplace 50 píxeles hacia la derecha y 50 píxeles hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="eff97-245">The illustration on the right shows the result of transforming the **ID2D1BitmapBrush** so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="eff97-246">El mapa de bits ahora rellena el rectángulo.</span><span class="sxs-lookup"><span data-stu-id="eff97-246">The bitmap now fills the rectangle.</span></span>

![Ilustración de un cuadrado pintado con un pincel de mapa de bits sin transformar el pincel y transformando el pincel](images/brushes-ovw-transform.png)

<span data-ttu-id="eff97-248">En el código siguiente se muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="eff97-248">The following code shows how to accomplish this.</span></span> <span data-ttu-id="eff97-249">En primer lugar, aplique una traducción al [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moviendo el pincel 50 píxeles a lo largo del eje x y 50 píxeles hacia abajo a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="eff97-249">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="eff97-250">A continuación, use **ID2D1BitmapBrush** para rellenar el rectángulo que tiene la esquina superior izquierda en (100, 100) y la esquina inferior derecha en (200, 200).</span><span class="sxs-lookup"><span data-stu-id="eff97-250">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a><span data-ttu-id="eff97-251">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eff97-251">Related topics</span></span>

* [<span data-ttu-id="eff97-252">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="eff97-252">Direct2D reference</span></span>](reference.md)
* [<span data-ttu-id="eff97-253">Cómo crear un pincel de color sólido</span><span class="sxs-lookup"><span data-stu-id="eff97-253">How to create a solid color brush</span></span>](how-to-create-a-solid-color-brush.md)
* [<span data-ttu-id="eff97-254">Cómo crear un pincel de degradado lineal</span><span class="sxs-lookup"><span data-stu-id="eff97-254">How to create a linear gradient brush</span></span>](how-to-create-a-linear-gradient-brush.md)
* [<span data-ttu-id="eff97-255">Cómo crear un pincel de degradado radial</span><span class="sxs-lookup"><span data-stu-id="eff97-255">How to create a radial gradient brush</span></span>](how-to-create-a-radial-gradient-brush.md)
* [<span data-ttu-id="eff97-256">Cómo crear un pincel de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="eff97-256">How to create a bitmap brush</span></span>](how-to-create-a-bitmap-brush.md)
