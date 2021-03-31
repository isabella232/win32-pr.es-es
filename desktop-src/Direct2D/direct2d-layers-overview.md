---
title: Información general sobre capas
description: Describe los aspectos básicos de las capas de Direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, capas
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0e86b32296718a975ebabccd5fc4ef0ee30cf289
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995459"
---
# <a name="layers-overview"></a><span data-ttu-id="0a537-104">Información general sobre capas</span><span class="sxs-lookup"><span data-stu-id="0a537-104">Layers Overview</span></span>

<span data-ttu-id="0a537-105">En esta información general se describen los aspectos básicos del uso de capas de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="0a537-105">This overview describes the basics of using Direct2D layers.</span></span> <span data-ttu-id="0a537-106">Contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="0a537-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="0a537-107">¿Qué son las capas?</span><span class="sxs-lookup"><span data-stu-id="0a537-107">What Are Layers?</span></span>](#what-are-layers)
-   [<span data-ttu-id="0a537-108">Capas en Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="0a537-108">Layers in Windows 8 and later</span></span>](#layers-in-windows-8-and-later)
    -   [<span data-ttu-id="0a537-109">ID2D1DeviceContext y PushLayer</span><span class="sxs-lookup"><span data-stu-id="0a537-109">ID2D1DeviceContext and PushLayer</span></span>](#id2d1devicecontext-and-pushlayer)
    -   [<span data-ttu-id="0a537-110">Capa \_ D2D1 \_ PARAMETERS1 y \_ capa D2D1 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="0a537-110">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>](/windows)
    -   [<span data-ttu-id="0a537-111">Modos de fusión</span><span class="sxs-lookup"><span data-stu-id="0a537-111">Blend Modes</span></span>](#blend-modes)
    -   [<span data-ttu-id="0a537-112">Interoperación</span><span class="sxs-lookup"><span data-stu-id="0a537-112">Interoperation</span></span>](#interoperation)
-   [<span data-ttu-id="0a537-113">Crear capas</span><span class="sxs-lookup"><span data-stu-id="0a537-113">Creating Layers</span></span>](#creating-layers)
-   [<span data-ttu-id="0a537-114">Límites de contenido</span><span class="sxs-lookup"><span data-stu-id="0a537-114">Content Bounds</span></span>](#content-bounds)
-   [<span data-ttu-id="0a537-115">Máscaras geométricas</span><span class="sxs-lookup"><span data-stu-id="0a537-115">Geometric Masks</span></span>](#geometric-masks)
-   [<span data-ttu-id="0a537-116">Máscaras de opacidad</span><span class="sxs-lookup"><span data-stu-id="0a537-116">Opacity Masks</span></span>](#opacity-masks)
-   [<span data-ttu-id="0a537-117">Alternativas a las capas</span><span class="sxs-lookup"><span data-stu-id="0a537-117">Alternatives to Layers</span></span>](#alternatives-to-layers)
-   [<span data-ttu-id="0a537-118">Recortar una forma arbitraria</span><span class="sxs-lookup"><span data-stu-id="0a537-118">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="0a537-119">Clips alineados del eje</span><span class="sxs-lookup"><span data-stu-id="0a537-119">Axis aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="0a537-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a537-120">Related topics</span></span>](#related-topics)

## <a name="what-are-layers"></a><span data-ttu-id="0a537-121">¿Qué son las capas?</span><span class="sxs-lookup"><span data-stu-id="0a537-121">What Are Layers?</span></span>

<span data-ttu-id="0a537-122">Las capas, representadas por objetos [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , permiten a una aplicación manipular un grupo de operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="0a537-122">Layers, represented by [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) objects, enable an application to manipulate a group of drawing operations.</span></span> <span data-ttu-id="0a537-123">Use una capa "insértela" en un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="0a537-123">You use a layer by "pushing" it onto a render target.</span></span> <span data-ttu-id="0a537-124">Las operaciones de dibujo posteriores por el destino de representación se dirigen a la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-124">Subsequent drawing operations by the render target are directed to the layer.</span></span> <span data-ttu-id="0a537-125">Una vez que haya terminado con la capa, "extrae" la capa del destino de representación, que compone el contenido de la capa de nuevo en el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="0a537-125">After you're finished with the layer, you "pop" the layer from the render target, which composites the layer's content back to the render target.</span></span>

<span data-ttu-id="0a537-126">Como los pinceles, las capas son recursos dependientes del dispositivo creados por destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="0a537-126">Like brushes, layers are device-dependent resources created by render targets.</span></span> <span data-ttu-id="0a537-127">Las capas se pueden usar en cualquier destino de representación en el mismo dominio de recursos que contiene el destino de representación que la creó.</span><span class="sxs-lookup"><span data-stu-id="0a537-127">Layers can be used on any render target in the same resource domain that contains the render target that created it.</span></span> <span data-ttu-id="0a537-128">Sin embargo, un recurso de capa solo se puede usar en un destino de representación a la vez.</span><span class="sxs-lookup"><span data-stu-id="0a537-128">However, a layer resource can only be used by one render target at a time.</span></span> <span data-ttu-id="0a537-129">Para obtener más información acerca de los recursos, consulte [información general sobre recursos](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="0a537-129">For more information about resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="0a537-130">Aunque las capas ofrecen una técnica de representación eficaz para producir efectos interesantes, un número excesivo de capas en una aplicación puede afectar negativamente a su rendimiento, debido a los diversos costos asociados con la administración de capas y recursos de capas.</span><span class="sxs-lookup"><span data-stu-id="0a537-130">Although layers offer a powerful rendering technique for producing interesting effects, excessive number of layers in an application can adversely affect its performance, because of the various costs associated with managing layers and layer resources.</span></span> <span data-ttu-id="0a537-131">Por ejemplo, existe el costo de rellenar o borrar la capa y, a continuación, fusionarla de nuevo, en especial en el hardware de un extremo superior.</span><span class="sxs-lookup"><span data-stu-id="0a537-131">For example, there is the cost of filling or clearing the layer and then blending it back, especially on higher-end hardware.</span></span> <span data-ttu-id="0a537-132">Después, hay el costo de administrar los recursos de la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-132">Then, there is the cost of managing the layer resources.</span></span> <span data-ttu-id="0a537-133">Si se reasignan con frecuencia, las pausas resultantes en la GPU serán el problema más importante.</span><span class="sxs-lookup"><span data-stu-id="0a537-133">If you reallocate these frequently, the resulting stalls against the GPU will be the most significant problem.</span></span> <span data-ttu-id="0a537-134">Al diseñar la aplicación, intente maximizar la reutilización de los recursos de la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-134">When you design your application, try to maximize reusing layer resources.</span></span>

## <a name="layers-in-windows-8-and-later"></a><span data-ttu-id="0a537-135">Capas en Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="0a537-135">Layers in Windows 8 and later</span></span>

<span data-ttu-id="0a537-136">Windows 8 presentó nuevas API relacionadas con la capa que simplifican, mejoran el rendimiento y agregan características a las capas.</span><span class="sxs-lookup"><span data-stu-id="0a537-136">Windows 8 introduced new layer related APIs that simplify, improve the performance of, and add features to layers.</span></span>

### <a name="id2d1devicecontext-and-pushlayer"></a><span data-ttu-id="0a537-137">ID2D1DeviceContext y PushLayer</span><span class="sxs-lookup"><span data-stu-id="0a537-137">ID2D1DeviceContext and PushLayer</span></span>

<span data-ttu-id="0a537-138">La interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) se deriva de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) y es la clave para mostrar el contenido de Direct2D en Windows 8. para obtener más información sobre esta interfaz, consulte [dispositivos y contextos de dispositivos](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="0a537-138">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="0a537-139">Con la interfaz de contexto del dispositivo, puede omitir la llamada al método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y, a continuación, pasar null al método [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="0a537-139">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="0a537-140">Direct2D administra automáticamente el recurso de capa y puede compartir recursos entre capas y gráficos de efectos.</span><span class="sxs-lookup"><span data-stu-id="0a537-140">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a><span data-ttu-id="0a537-141">Capa \_ D2D1 \_ PARAMETERS1 y \_ capa D2D1 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="0a537-141">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>

<span data-ttu-id="0a537-142">La estructura D2D1 de la [**\_ capa \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) es igual que los parámetros de la [**\_ capa \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), salvo que el miembro final de la estructura es ahora una enumeración [**\_ \_ OPTIONS1 de nivel D2D1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) .</span><span class="sxs-lookup"><span data-stu-id="0a537-142">The [**D2D1\_LAYER\_PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) structure is the same as [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), except the final member of the structure is now a [**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) enumeration.</span></span>

<span data-ttu-id="0a537-143">[**D2D1 \_ La capa \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) no tiene la opción ClearType y tiene dos opciones diferentes que puede usar para mejorar el rendimiento:</span><span class="sxs-lookup"><span data-stu-id="0a537-143">[**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) has no ClearType option and has two different options that you can use to improve performance:</span></span>

-   <span data-ttu-id="0a537-144">[**D2D1 \_ La \_ OPTIONS1 \_ de capa se inicializa \_ desde el \_ fondo**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D representa los primitivos en la capa sin borrarlos con negro transparente.</span><span class="sxs-lookup"><span data-stu-id="0a537-144">[**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renders primitives to the layer without clearing it with transparent black.</span></span> <span data-ttu-id="0a537-145">Este no es el valor predeterminado, pero en la mayoría de los casos resulta en un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0a537-145">This is not the default, but in most cases results in better performance.</span></span>

-   <span data-ttu-id="0a537-146">[**D2D1 \_ NIVEL \_ OPTIONS1 \_ Ignore \_ Alpha**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Si la superficie subyacente se establece en [**D2D1 \_ en \_ modo \_ alfa**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), esta opción permite a Direct2D evitar modificar el canal alfa de la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-146">[**D2D1\_LAYER\_OPTIONS1\_IGNORE\_ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): if the underlying surface is set to [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), this option lets Direct2D avoid modifying the alpha channel of the layer.</span></span> <span data-ttu-id="0a537-147">No lo use en otros casos.</span><span class="sxs-lookup"><span data-stu-id="0a537-147">Do not use this in other cases.</span></span>

### <a name="blend-modes"></a><span data-ttu-id="0a537-148">Modos de fusión</span><span class="sxs-lookup"><span data-stu-id="0a537-148">Blend Modes</span></span>

<span data-ttu-id="0a537-149">A partir de Windows 8, el contexto de dispositivo tiene un [**modo de mezcla primitivo**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) que determina cómo se mezcla cada primitivo con la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="0a537-149">Starting in Windows 8, the device context has a [**primitive blend mode**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) that determines how each primitive is blended with the target surface.</span></span> <span data-ttu-id="0a537-150">Este modo también se aplica a las capas cuando se llama al método [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="0a537-150">This mode also applies to layers when you call the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span>

<span data-ttu-id="0a537-151">Por ejemplo, si usa una capa para recortar los primitivos con transparencia, establezca el modo de [**copia de D2D1 \_ primitiva \_ Blend \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) en el contexto del dispositivo para obtener los resultados correctos.</span><span class="sxs-lookup"><span data-stu-id="0a537-151">For example, if you are using a layer to clip primitives with transparency set the [**D2D1\_PRIMITIVE\_BLEND\_COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) mode on the device context for proper results.</span></span> <span data-ttu-id="0a537-152">El modo de copia hace que el contexto de dispositivo sea lineal interpolación de los 4 canales de color, incluido el canal alfa, de cada píxel con el contenido de la superficie de destino según la máscara geométrica de la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-152">The copy mode makes the device context linear interpolate all 4 color channels, including the alpha channel, of each pixel with the contents of the target surface according to the geometric mask of the layer.</span></span>

### <a name="interoperation"></a><span data-ttu-id="0a537-153">Interoperación</span><span class="sxs-lookup"><span data-stu-id="0a537-153">Interoperation</span></span>

<span data-ttu-id="0a537-154">A partir de Windows 8, Direct2D admite la interoperación con Direct3D y GDI mientras se inserta una capa o un clip.</span><span class="sxs-lookup"><span data-stu-id="0a537-154">Starting in Windows 8, Direct2D supports interoperation with Direct3D and GDI while a layer or clip is pushed.</span></span> <span data-ttu-id="0a537-155">Se llama a [**ID2D1GdiInteropRenderTarget:: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) mientras se inserta una capa para interoperar con GDI.</span><span class="sxs-lookup"><span data-stu-id="0a537-155">You call [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) while a layer is pushed to interoperate with GDI.</span></span> <span data-ttu-id="0a537-156">Se llama a [**ID2D1DeviceContext:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) y después se representa en la superficie subyacente para interoperar con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0a537-156">You call [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) and then render to the underlying surface to interoperate with Direct3D.</span></span> <span data-ttu-id="0a537-157">Es su responsabilidad representar dentro de la capa o el clip con Direct3D o GDI.</span><span class="sxs-lookup"><span data-stu-id="0a537-157">It is your responsibility to render inside the layer or clip with Direct3D or GDI.</span></span> <span data-ttu-id="0a537-158">Si intenta representar fuera de la capa o recortar, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="0a537-158">If you try to render outside the layer or clip the results are undefined.</span></span>

## <a name="creating-layers"></a><span data-ttu-id="0a537-159">Crear capas</span><span class="sxs-lookup"><span data-stu-id="0a537-159">Creating Layers</span></span>

<span data-ttu-id="0a537-160">Para trabajar con capas es necesario estar familiarizado con los métodos [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))y [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , y con la estructura de [**\_ \_ parámetros de capa D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , que contiene un conjunto de datos paramétricos que define cómo se puede usar la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-160">Working with layers requires familiarity with the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) methods, and the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure, which contains a set of parametric data that defines how the layer can be used.</span></span> <span data-ttu-id="0a537-161">En la lista siguiente se describen los métodos y la estructura.</span><span class="sxs-lookup"><span data-stu-id="0a537-161">The following list describes the methods and structure.</span></span>

-   <span data-ttu-id="0a537-162">Llame al método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para crear un recurso de capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-162">Call the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method to create a layer resource.</span></span>
    > [!Note]  
    > <span data-ttu-id="0a537-163">A partir de Windows 8, puede omitir la llamada al método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y, a continuación, pasar null al método [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) en la interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="0a537-163">Starting in Windows 8, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface.</span></span> <span data-ttu-id="0a537-164">Esto es más sencillo y permite a Direct2D administrar automáticamente el recurso de capa y compartir recursos entre capas y gráficos de efectos.</span><span class="sxs-lookup"><span data-stu-id="0a537-164">This is simpler and allows Direct2D to automatically manage the layer resource and share resources between layers and effect graphs.</span></span>

     

-   <span data-ttu-id="0a537-165">Después de que el destino de representación haya empezado a dibujar (después de que se haya llamado al método [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) ), puede usar el método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="0a537-165">After render target has begun drawing (after its [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method has been called), you can use the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="0a537-166">El método **PushLayer** agrega la capa especificada al destino de representación, de modo que el destino recibe todas las operaciones de dibujo posteriores hasta que se llama a [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="0a537-166">The **PushLayer** method adds the specified layer to the render target, so that the target receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <span data-ttu-id="0a537-167">Este método toma un objeto [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) devuelto mediante una llamada a [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y un *layerParameters* en la estructura de [**\_ \_ parámetros de nivel D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="0a537-167">This method takes an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) object returned by calling [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) and an *layerParameters* in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure.</span></span> <span data-ttu-id="0a537-168">En la tabla siguiente se describen los campos de la estructura.</span><span class="sxs-lookup"><span data-stu-id="0a537-168">The following table describes the fields of the structure.</span></span> 

    | <span data-ttu-id="0a537-169">Campo</span><span class="sxs-lookup"><span data-stu-id="0a537-169">Field</span></span>                 | <span data-ttu-id="0a537-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a537-170">Description</span></span>                                                                                                                                                                                                                                                                 |     |
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
    | <span data-ttu-id="0a537-171">**contentBounds**</span><span class="sxs-lookup"><span data-stu-id="0a537-171">**contentBounds**</span></span>     | <span data-ttu-id="0a537-172">Los límites de contenido de la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-172">The content bounds of the layer.</span></span> <span data-ttu-id="0a537-173">Se garantiza que el contenido que se encuentra fuera de estos límites no se representa.</span><span class="sxs-lookup"><span data-stu-id="0a537-173">Content outside these bounds is guaranteed not to render.</span></span> <span data-ttu-id="0a537-174">El valor predeterminado de este parámetro es [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span><span class="sxs-lookup"><span data-stu-id="0a537-174">This parameter defaults to [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span></span> <span data-ttu-id="0a537-175">Cuando se usa el valor predeterminado, los límites del contenido se toman en efecto para ser los límites del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="0a537-175">When the default value is used, the content bounds are effectively taken to be the bounds of the render target.</span></span> |     |
    | <span data-ttu-id="0a537-176">**geometricMask**</span><span class="sxs-lookup"><span data-stu-id="0a537-176">**geometricMask**</span></span>     | <span data-ttu-id="0a537-177">Opta Área, definida por un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), a la que se debe recortar la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-177">(Optional) The area, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), to which the layer should be clipped.</span></span> <span data-ttu-id="0a537-178">Se establece en **null** si la capa no debe recortarse en una geometría.</span><span class="sxs-lookup"><span data-stu-id="0a537-178">Set to **NULL** if the layer shouldn't be clipped to a geometry.</span></span>                                                                                           |     |
    | <span data-ttu-id="0a537-179">**maskAntialiasMode**</span><span class="sxs-lookup"><span data-stu-id="0a537-179">**maskAntialiasMode**</span></span> | <span data-ttu-id="0a537-180">Valor que especifica el modo de suavizado de contorno de la máscara geométrica especificada por el campo **geometricMask** .</span><span class="sxs-lookup"><span data-stu-id="0a537-180">A value that specifies the antialiasing mode for the geometric mask specified by the **geometricMask** field.</span></span>                                                                                                                                                               |     |
    | <span data-ttu-id="0a537-181">**maskTransform**</span><span class="sxs-lookup"><span data-stu-id="0a537-181">**maskTransform**</span></span>     | <span data-ttu-id="0a537-182">Valor que especifica la transformación que se aplica a la máscara geométrica al crear la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-182">A value that specifies the transform that is applied to the geometric mask when composing the layer.</span></span> <span data-ttu-id="0a537-183">Esto es relativo a la transformación del mundo.</span><span class="sxs-lookup"><span data-stu-id="0a537-183">This is relative to the world transform.</span></span>                                                                                                                               |     |
    | <span data-ttu-id="0a537-184">**opacidad**</span><span class="sxs-lookup"><span data-stu-id="0a537-184">**opacity**</span></span>           | <span data-ttu-id="0a537-185">Valor de opacidad de la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-185">The opacity value of the layer.</span></span> <span data-ttu-id="0a537-186">La opacidad de cada recurso de la capa se multiplica por este valor al componerlo en el destino.</span><span class="sxs-lookup"><span data-stu-id="0a537-186">The opacity of each resource in the layer is multiplied with this value when compositing to the target.</span></span>                                                                                                                                     |     |
    | <span data-ttu-id="0a537-187">**opacityBrush**</span><span class="sxs-lookup"><span data-stu-id="0a537-187">**opacityBrush**</span></span>      | <span data-ttu-id="0a537-188">Opta Pincel que se usa para modificar la opacidad de la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-188">(Optional) A brush that is used to modify the opacity of the layer.</span></span> <span data-ttu-id="0a537-189">El pincel se asigna a la capa y el canal alfa de cada píxel del pincel asignado se multiplica por el píxel de capa correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0a537-189">The brush is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.</span></span> <span data-ttu-id="0a537-190">Se establece en **null** si la capa no debe tener una máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="0a537-190">Set to **NULL** if the layer shouldn't have an opacity mask.</span></span>    |     |
    | <span data-ttu-id="0a537-191">**layerOptions**</span><span class="sxs-lookup"><span data-stu-id="0a537-191">**layerOptions**</span></span>      | <span data-ttu-id="0a537-192">Valor que especifica si la capa va a representar texto con suavizado de contorno de ClearType.</span><span class="sxs-lookup"><span data-stu-id="0a537-192">A value that specifies whether the layer intends to render text with ClearType antialiasing.</span></span> <span data-ttu-id="0a537-193">El valor predeterminado de este parámetro es OFF.</span><span class="sxs-lookup"><span data-stu-id="0a537-193">This parameter defaults to off.</span></span> <span data-ttu-id="0a537-194">Al activarlo, se permite que ClearType funcione correctamente, pero se produce una velocidad de representación ligeramente más lenta.</span><span class="sxs-lookup"><span data-stu-id="0a537-194">Turning it on enables ClearType to work correctly, but it results in slightly slower rendering speed.</span></span>                                          |     |

    

     

    > [!Note]  
    > <span data-ttu-id="0a537-195">A partir de Windows 8, no se puede representar con ClearType en una capa, por lo que el parámetro **layerOptions** siempre debe establecerse en [**D2D1 \_ Layer \_ Options \_ None**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span><span class="sxs-lookup"><span data-stu-id="0a537-195">Starting in Windows 8, you cannot render with ClearType in a layer, so the **layerOptions** parameter should always be set to [**D2D1\_LAYER\_OPTIONS\_NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span></span>

     

    <span data-ttu-id="0a537-196">Para mayor comodidad, Direct2D proporciona el método [**D2D1:: LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) para ayudarle a crear estructuras de [**\_ \_ parámetros de capa D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="0a537-196">For convenience, Direct2D provides the [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) method to help you create [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structures.</span></span>

-   <span data-ttu-id="0a537-197">Para componer el contenido de la capa en el destino de representación, llame al método [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="0a537-197">To composite the contents of the layer into the render target, call the [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) method.</span></span> <span data-ttu-id="0a537-198">Debe llamar al método **PopLayer** antes de llamar al método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="0a537-198">You must call the **PopLayer** method before you call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span>

<span data-ttu-id="0a537-199">En el ejemplo siguiente se muestra cómo usar [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))y [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span><span class="sxs-lookup"><span data-stu-id="0a537-199">The following example shows how to use [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span></span> <span data-ttu-id="0a537-200">Todos los campos de la estructura de [**\_ \_ parámetros de nivel D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) se establecen en sus valores predeterminados, excepto **opacityBrush**, que se establece en [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="0a537-200">All fields in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to their defaults, except **opacityBrush**, which is set to an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



<span data-ttu-id="0a537-201">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0a537-201">Code has been omitted from this example.</span></span>

<span data-ttu-id="0a537-202">Tenga en cuenta que al llamar a [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) y [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), asegúrese de que cada **PushLayer** tiene una llamada **PopLayer** coincidente.</span><span class="sxs-lookup"><span data-stu-id="0a537-202">Note that when you call [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ensure that each **PushLayer** has a matching **PopLayer** call.</span></span> <span data-ttu-id="0a537-203">Si hay más llamadas a **PopLayer** que llamadas a **PushLayer** , el destino de representación se coloca en un estado de error.</span><span class="sxs-lookup"><span data-stu-id="0a537-203">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="0a537-204">Si se llama a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) antes de que se extraigan todos los niveles pendientes, el destino de representación se coloca en un estado de error y devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="0a537-204">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state and returns an error.</span></span> <span data-ttu-id="0a537-205">Para borrar el estado de error, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="0a537-205">To clear the error state, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

## <a name="content-bounds"></a><span data-ttu-id="0a537-206">Límites de contenido</span><span class="sxs-lookup"><span data-stu-id="0a537-206">Content Bounds</span></span>

<span data-ttu-id="0a537-207">**ContentBounds** establece el límite de lo que se va a dibujar en la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-207">The **contentBounds** sets the limit of what is to be drawn to the layer.</span></span> <span data-ttu-id="0a537-208">Solo los elementos de los límites de contenido se componen de nuevo en el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="0a537-208">Only those things within the content bounds are composited back to the render target.</span></span>

<span data-ttu-id="0a537-209">En el ejemplo siguiente se muestra cómo especificar **contentBounds** para que la imagen original se recorte en los límites de contenido con la esquina superior izquierda en (10, 108) y la esquina inferior derecha en (121, 177).</span><span class="sxs-lookup"><span data-stu-id="0a537-209">The example that follows shows how to specify **contentBounds** so that the original image is clipped to the content bounds with the upper-left corner at (10, 108) and the lower-right corner at (121, 177).</span></span> <span data-ttu-id="0a537-210">En la ilustración siguiente se muestra la imagen original y el resultado de recortar la imagen en los límites de contenido.</span><span class="sxs-lookup"><span data-stu-id="0a537-210">The following illustration shows the original image and the result of clipping the image to the content bounds.</span></span>

![Ilustración de los límites de contenido en una imagen original y la imagen recortada resultante](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="0a537-212">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0a537-212">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="0a537-213">La imagen recortada resultante se ve afectada aún más si se especifica un **geometricMask**.</span><span class="sxs-lookup"><span data-stu-id="0a537-213">The resulting clipped image is further affected if you specify a **geometricMask**.</span></span> <span data-ttu-id="0a537-214">Vea la sección [máscaras geométricas](#geometric-masks) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0a537-214">See the [Geometric Masks](#geometric-masks) section for more information.</span></span>

 

## <a name="geometric-masks"></a><span data-ttu-id="0a537-215">Máscaras geométricas</span><span class="sxs-lookup"><span data-stu-id="0a537-215">Geometric Masks</span></span>

<span data-ttu-id="0a537-216">Una máscara geométrica es un clip o un recorte, definido por un objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , que enmascara una capa cuando se dibuja mediante un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="0a537-216">A geometric mask is a clip or a cutout, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="0a537-217">Puede usar el campo **geometricMask** de la estructura [**de \_ \_ parámetros de nivel D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) para enmascarar los resultados en una geometría.</span><span class="sxs-lookup"><span data-stu-id="0a537-217">You can use the **geometricMask** field of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to mask the results to a geometry.</span></span> <span data-ttu-id="0a537-218">Por ejemplo, si desea mostrar una imagen enmascarada por una letra de bloque "A", puede crear primero una geometría que represente la letra de bloque "A" y utilizar esa geometría como una máscara geométrica para una capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-218">For example, if you want to display an image masked by a block letter "A", you can first create a geometry representing the block letter "A" and use that geometry as a geometric mask for a layer.</span></span> <span data-ttu-id="0a537-219">Después, después de insertar la capa, puede dibujar la imagen.</span><span class="sxs-lookup"><span data-stu-id="0a537-219">Then, after pushing the layer, you can draw the image.</span></span> <span data-ttu-id="0a537-220">Al extraer la capa, la imagen se recorta en la forma "A" de la letra de bloque.</span><span class="sxs-lookup"><span data-stu-id="0a537-220">Popping the layer results in the image being clipped to the block letter "A" shape.</span></span>

<span data-ttu-id="0a537-221">En el ejemplo siguiente se muestra cómo crear un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) que contiene una forma de una montaña y después pasar la geometría de la ruta de acceso a [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="0a537-221">The example that follows shows how to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) containing a shape of a mountain and then pass the path geometry to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span></span> <span data-ttu-id="0a537-222">A continuación, dibuja un mapa de bits y los cuadrados.</span><span class="sxs-lookup"><span data-stu-id="0a537-222">It then draws a bitmap and squares.</span></span> <span data-ttu-id="0a537-223">Si solo hay un mapa de bits en la capa que se va a representar, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de mapa de bits con compresión para mayor eficacia.</span><span class="sxs-lookup"><span data-stu-id="0a537-223">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="0a537-224">En la siguiente ilustración se muestra el resultado del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0a537-224">The following illustration shows the output from the example.</span></span>

![Ilustración de una imagen de una hoja y la imagen resultante después de aplicar una máscara geométrica de una montaña](images/layers-bitmapmask.png)

<span data-ttu-id="0a537-226">En el primer ejemplo se define la geometría que se va a utilizar como máscara.</span><span class="sxs-lookup"><span data-stu-id="0a537-226">The first example defines the geometry to be used as a mask.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



<span data-ttu-id="0a537-227">En el ejemplo siguiente se utiliza la geometría como una máscara para la capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-227">The next example uses the geometry as a mask for the layer.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="0a537-228">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0a537-228">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="0a537-229">En general, si especifica un **geometricMask**, puede usar el valor predeterminado, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), para **contentBounds**.</span><span class="sxs-lookup"><span data-stu-id="0a537-229">In general, if you specify a **geometricMask**, you can use the default value, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), for the **contentBounds**.</span></span>
>
> <span data-ttu-id="0a537-230">Si **contentBounds** es NULL y **GEOMETRICMASK** no es null, los límites de contenido son, de hecho, los límites de la máscara geométrica después de aplicar la transformación de máscara.</span><span class="sxs-lookup"><span data-stu-id="0a537-230">If **contentBounds** is NULL, and **geometricMask** is non-NULL, then the content bounds are effectively the bounds of the geometric mask after the mask transform is applied.</span></span>
>
> <span data-ttu-id="0a537-231">Si **contentBounds** no es NULL y **GEOMETRICMASK** no es null, la máscara geométrica transformada se recorta en efecto con los límites de contenido y se supone que los límites del contenido son infinitos.</span><span class="sxs-lookup"><span data-stu-id="0a537-231">If **contentBounds** is non-NULL, and **geometricMask** is non-NULL, then the transformed geometric mask is effectively clipped against content bounds and the content bounds are assumed to be infinite.</span></span>

 

## <a name="opacity-masks"></a><span data-ttu-id="0a537-232">Máscaras de opacidad</span><span class="sxs-lookup"><span data-stu-id="0a537-232">Opacity Masks</span></span>

<span data-ttu-id="0a537-233">Una máscara de opacidad es una máscara, descrita por un pincel o mapa de bits, que se aplica a otro objeto para hacer que ese objeto sea parcial o completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="0a537-233">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="0a537-234">Permite el uso del canal alfa de un pincel para usarse como máscara de contenido.</span><span class="sxs-lookup"><span data-stu-id="0a537-234">It allows the use of the alpha channel of a brush to be used as a content mask.</span></span> <span data-ttu-id="0a537-235">Por ejemplo, puede definir un pincel de degradado radial que varíe de opaco a transparente para crear un efecto de viñetas.</span><span class="sxs-lookup"><span data-stu-id="0a537-235">For example, you can define a radial gradient brush that varies from opaque to transparent to create a vignette effect.</span></span>

<span data-ttu-id="0a537-236">En el ejemplo siguiente se usa un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) como máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="0a537-236">The example that follows uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m\_pRadialGradientBrush*) as an opacity mask.</span></span> <span data-ttu-id="0a537-237">A continuación, dibuja un mapa de bits y los cuadrados.</span><span class="sxs-lookup"><span data-stu-id="0a537-237">It then draws a bitmap and squares.</span></span> <span data-ttu-id="0a537-238">Si solo hay un mapa de bits en la capa que se va a representar, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de mapa de bits con compresión para mayor eficacia.</span><span class="sxs-lookup"><span data-stu-id="0a537-238">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="0a537-239">En la ilustración siguiente se muestra el resultado de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0a537-239">The following illustration shows the output from this example.</span></span>

![Ilustración de una imagen de árboles y la imagen resultante después de aplicar una máscara de opacidad](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="0a537-241">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0a537-241">Code has been omitted from this example.</span></span>

> [!Note]  
> <span data-ttu-id="0a537-242">En este ejemplo se usa una capa para aplicar una máscara de opacidad a un solo objeto con el fin de que el ejemplo sea lo más sencillo posible.</span><span class="sxs-lookup"><span data-stu-id="0a537-242">This example uses a layer to apply an opacity mask to a single object to keep the example as simple as possible.</span></span> <span data-ttu-id="0a537-243">Al aplicar una máscara de opacidad a un solo objeto, resulta más eficaz usar los métodos [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) o [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , en lugar de una capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-243">When applying an opacity mask to a single object, its more efficient to use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) or [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods, rather than a layer.</span></span>

 

<span data-ttu-id="0a537-244">Para obtener instrucciones sobre cómo aplicar una máscara de opacidad sin usar una capa, vea la [información general sobre las máscaras de opacidad](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a537-244">For instructions on how to apply an opacity mask without using a layer, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="alternatives-to-layers"></a><span data-ttu-id="0a537-245">Alternativas a las capas</span><span class="sxs-lookup"><span data-stu-id="0a537-245">Alternatives to Layers</span></span>

<span data-ttu-id="0a537-246">Como se mencionó anteriormente, un número excesivo de capas puede afectar negativamente al rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a537-246">As mentioned earlier, excessive number of layers can adversely affect the performance of your application.</span></span> <span data-ttu-id="0a537-247">Para mejorar el rendimiento, evite el uso de capas siempre que sea posible. en su lugar, use sus alternativas.</span><span class="sxs-lookup"><span data-stu-id="0a537-247">To improve performance, avoid using layers whenever possible; instead use their alternatives.</span></span> <span data-ttu-id="0a537-248">En el ejemplo de código siguiente se muestra cómo usar [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) y [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para recortar una región, como alternativa al uso de una capa con límites de contenido.</span><span class="sxs-lookup"><span data-stu-id="0a537-248">The following code example shows how to use [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to clip a region, as an alternative to using a layer with content bounds.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



<span data-ttu-id="0a537-249">Del mismo modo, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de mapa de bits con compresión como alternativa al uso de una capa con una máscara de opacidad cuando solo hay un contenido en la capa que se va a representar, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="0a537-249">Similarly, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush as an alternative to using a layer with an opacity mask when there is only one content in the layer to render, as shown in the following example.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



<span data-ttu-id="0a537-250">Como alternativa al uso de una capa con una máscara geométrica, considere la posibilidad de usar una máscara de mapa de bits para recortar una región, tal y como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="0a537-250">As an alternative to using a layer with a geometric mask, consider using a bitmap mask to clip a region, as shown in the following example.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="0a537-251">Por último, si desea aplicar la opacidad a un solo primitivo, debe multiplicar la opacidad en el color del pincel y, a continuación, representar el primitivo.</span><span class="sxs-lookup"><span data-stu-id="0a537-251">Lastly, if you want to apply opacity to a single primitive, you should multiply the opacity into the into the brush color and then render the primitive.</span></span> <span data-ttu-id="0a537-252">No necesita una capa o un mapa de bits de máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="0a537-252">You do not need a layer or an opacity mask bitmap.</span></span>


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="0a537-253">Recortar una forma arbitraria</span><span class="sxs-lookup"><span data-stu-id="0a537-253">Clipping an arbitrary shape</span></span>

<span data-ttu-id="0a537-254">En la ilustración siguiente se muestra el resultado de aplicar un clip a una imagen.</span><span class="sxs-lookup"><span data-stu-id="0a537-254">The figure here shows the result of applying a clip to an image.</span></span>

![imagen que muestra un ejemplo de una imagen antes y después de un clip.](images/clip.png)

<span data-ttu-id="0a537-256">Puede obtener este resultado mediante el uso de capas con una máscara de geometría o el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de opacidad.</span><span class="sxs-lookup"><span data-stu-id="0a537-256">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="0a537-257">A continuación se muestra un ejemplo en el que se usa una capa:</span><span class="sxs-lookup"><span data-stu-id="0a537-257">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="0a537-258">Este es un ejemplo que usa el método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :</span><span class="sxs-lookup"><span data-stu-id="0a537-258">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



<span data-ttu-id="0a537-259">En este ejemplo de código, cuando se llama al método PushLayer, no se pasa una capa creada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a537-259">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="0a537-260">Direct2D crea una capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-260">Direct2D creates a layer for you.</span></span> <span data-ttu-id="0a537-261">Direct2D es capaz de administrar la asignación y destrucción de este recurso sin ninguna implicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0a537-261">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="0a537-262">Esto permite a Direct2D volver a usar las capas internamente y aplicar optimizaciones de administración de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a537-262">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

> [!Note]  
> <span data-ttu-id="0a537-263">En Windows 8 se han realizado muchas optimizaciones para el uso de capas y se recomienda intentar usar las API de capa en lugar de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="0a537-263">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

 

### <a name="axis-aligned-clips"></a><span data-ttu-id="0a537-264">Clips alineados del eje</span><span class="sxs-lookup"><span data-stu-id="0a537-264">Axis aligned clips</span></span>

<span data-ttu-id="0a537-265">Si la región que se va a recortar se alinea con el eje de la superficie de dibujo, en lugar de arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0a537-265">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="0a537-266">Este caso es adecuado para usar un rectángulo de recorte en lugar de una capa.</span><span class="sxs-lookup"><span data-stu-id="0a537-266">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="0a537-267">La ganancia de rendimiento es más para la geometría con alias que la geometría con suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="0a537-267">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="0a537-268">Para obtener más información sobre los clips alineados del eje, vea el tema [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .</span><span class="sxs-lookup"><span data-stu-id="0a537-268">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a537-269">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a537-269">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a537-270">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="0a537-270">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 