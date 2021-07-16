---
title: Información general sobre capas
description: Describe los conceptos básicos de las capas de Direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, capas
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 027be097c5c21929f3ccdbaa169a1f3dac55b394
ms.sourcegitcommit: 698ce2d9ba2fa650f2875225d99623995fac246a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2021
ms.locfileid: "114231612"
---
# <a name="layers-overview"></a><span data-ttu-id="d9001-104">Información general sobre capas</span><span class="sxs-lookup"><span data-stu-id="d9001-104">Layers Overview</span></span>

<span data-ttu-id="d9001-105">En esta introducción se describen los conceptos básicos del uso de capas de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="d9001-105">This overview describes the basics of using Direct2D layers.</span></span> <span data-ttu-id="d9001-106">Contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="d9001-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="d9001-107">¿Qué son las capas?</span><span class="sxs-lookup"><span data-stu-id="d9001-107">What Are Layers?</span></span>](#what-are-layers)
-   [<span data-ttu-id="d9001-108">Capas en Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="d9001-108">Layers in Windows 8 and later</span></span>](#layers-in-windows-8-and-later)
    -   [<span data-ttu-id="d9001-109">ID2D1DeviceContext y PushLayer</span><span class="sxs-lookup"><span data-stu-id="d9001-109">ID2D1DeviceContext and PushLayer</span></span>](#id2d1devicecontext-and-pushlayer)
    -   [<span data-ttu-id="d9001-110">D2D1 \_ LAYER \_ PARAMETERS1 y D2D1 \_ LAYER \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="d9001-110">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>](/windows)
    -   [<span data-ttu-id="d9001-111">Modos de fusión</span><span class="sxs-lookup"><span data-stu-id="d9001-111">Blend Modes</span></span>](#blend-modes)
    -   [<span data-ttu-id="d9001-112">Interoperación</span><span class="sxs-lookup"><span data-stu-id="d9001-112">Interoperation</span></span>](#interoperation)
-   [<span data-ttu-id="d9001-113">Creación de capas</span><span class="sxs-lookup"><span data-stu-id="d9001-113">Creating Layers</span></span>](#creating-layers)
-   [<span data-ttu-id="d9001-114">Límites de contenido</span><span class="sxs-lookup"><span data-stu-id="d9001-114">Content Bounds</span></span>](#content-bounds)
-   [<span data-ttu-id="d9001-115">Máscaras geométricas</span><span class="sxs-lookup"><span data-stu-id="d9001-115">Geometric Masks</span></span>](#geometric-masks)
-   [<span data-ttu-id="d9001-116">Máscaras de opacidad</span><span class="sxs-lookup"><span data-stu-id="d9001-116">Opacity Masks</span></span>](#opacity-masks)
-   [<span data-ttu-id="d9001-117">Alternativas a las capas</span><span class="sxs-lookup"><span data-stu-id="d9001-117">Alternatives to Layers</span></span>](#alternatives-to-layers)
-   [<span data-ttu-id="d9001-118">Recorte de una forma arbitraria</span><span class="sxs-lookup"><span data-stu-id="d9001-118">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="d9001-119">Clips alineados en el eje</span><span class="sxs-lookup"><span data-stu-id="d9001-119">Axis aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="d9001-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9001-120">Related topics</span></span>](#related-topics)

## <a name="what-are-layers"></a><span data-ttu-id="d9001-121">¿Qué son las capas?</span><span class="sxs-lookup"><span data-stu-id="d9001-121">What Are Layers?</span></span>

<span data-ttu-id="d9001-122">Las capas, representadas [**por objetos ID2D1Layer,**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) permiten a una aplicación manipular un grupo de operaciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="d9001-122">Layers, represented by [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) objects, enable an application to manipulate a group of drawing operations.</span></span> <span data-ttu-id="d9001-123">Para usar una capa, "insertarla" en un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="d9001-123">You use a layer by "pushing" it onto a render target.</span></span> <span data-ttu-id="d9001-124">Las operaciones de dibujo posteriores del destino de representación se dirigen a la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-124">Subsequent drawing operations by the render target are directed to the layer.</span></span> <span data-ttu-id="d9001-125">Cuando haya terminado con la capa, "resalte" la capa del destino de representación, que compone el contenido de la capa de nuevo al destino de representación.</span><span class="sxs-lookup"><span data-stu-id="d9001-125">After you're finished with the layer, you "pop" the layer from the render target, which composites the layer's content back to the render target.</span></span>

<span data-ttu-id="d9001-126">Al igual que los pinceles, las capas son recursos dependientes del dispositivo creados por destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="d9001-126">Like brushes, layers are device-dependent resources created by render targets.</span></span> <span data-ttu-id="d9001-127">Las capas se pueden usar en cualquier destino de representación en el mismo dominio de recursos que contiene el destino de representación que lo creó.</span><span class="sxs-lookup"><span data-stu-id="d9001-127">Layers can be used on any render target in the same resource domain that contains the render target that created it.</span></span> <span data-ttu-id="d9001-128">Sin embargo, un recurso de capa solo puede ser utilizado por un destino de representación a la vez.</span><span class="sxs-lookup"><span data-stu-id="d9001-128">However, a layer resource can only be used by one render target at a time.</span></span> <span data-ttu-id="d9001-129">Para obtener más información sobre los recursos, vea Información [general sobre recursos.](resources-and-resource-domains.md)</span><span class="sxs-lookup"><span data-stu-id="d9001-129">For more information about resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="d9001-130">Aunque las capas ofrecen una técnica de representación eficaz para producir efectos interesantes, un número excesivo de capas en una aplicación puede afectar negativamente a su rendimiento, debido a los distintos costos asociados con la administración de capas y recursos de capas.</span><span class="sxs-lookup"><span data-stu-id="d9001-130">Although layers offer a powerful rendering technique for producing interesting effects, excessive number of layers in an application can adversely affect its performance, because of the various costs associated with managing layers and layer resources.</span></span> <span data-ttu-id="d9001-131">Por ejemplo, existe el costo de rellenar o borrar la capa y, a continuación, combinarla de nuevo, especialmente en hardware de gama superior.</span><span class="sxs-lookup"><span data-stu-id="d9001-131">For example, there is the cost of filling or clearing the layer and then blending it back, especially on higher-end hardware.</span></span> <span data-ttu-id="d9001-132">A continuación, existe el costo de administrar los recursos de la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-132">Then, there is the cost of managing the layer resources.</span></span> <span data-ttu-id="d9001-133">Si los resigna con frecuencia, los detenciones resultantes en la GPU serán el problema más importante.</span><span class="sxs-lookup"><span data-stu-id="d9001-133">If you reallocate these frequently, the resulting stalls against the GPU will be the most significant problem.</span></span> <span data-ttu-id="d9001-134">Al diseñar la aplicación, intente maximizar la utilización de recursos de capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-134">When you design your application, try to maximize reusing layer resources.</span></span>

## <a name="layers-in-windows-8-and-later"></a><span data-ttu-id="d9001-135">Capas en Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="d9001-135">Layers in Windows 8 and later</span></span>

<span data-ttu-id="d9001-136">Windows 8 nuevas API relacionadas con capas que simplifican, mejoran el rendimiento de y agregan características a las capas.</span><span class="sxs-lookup"><span data-stu-id="d9001-136">Windows 8 introduced new layer related APIs that simplify, improve the performance of, and add features to layers.</span></span>

### <a name="id2d1devicecontext-and-pushlayer"></a><span data-ttu-id="d9001-137">ID2D1DeviceContext y PushLayer</span><span class="sxs-lookup"><span data-stu-id="d9001-137">ID2D1DeviceContext and PushLayer</span></span>

<span data-ttu-id="d9001-138">La interfaz [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) se deriva de la interfaz [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) y es clave para mostrar contenido de Direct2D en Windows 8. Para obtener más información sobre esta interfaz, vea Dispositivos y [contextos de dispositivo.](devices-and-device-contexts.md)</span><span class="sxs-lookup"><span data-stu-id="d9001-138">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="d9001-139">Con la interfaz de contexto del dispositivo, puede omitir la llamada al método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y, a continuación, pasar NULL al [**método ID2D1DeviceContext::P ushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="d9001-139">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="d9001-140">Direct2D administra automáticamente el recurso de capa y puede compartir recursos entre capas y gráficos de efectos.</span><span class="sxs-lookup"><span data-stu-id="d9001-140">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a><span data-ttu-id="d9001-141">D2D1 \_ LAYER \_ PARAMETERS1 y D2D1 \_ LAYER \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="d9001-141">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>

<span data-ttu-id="d9001-142">La [**estructura D2D1 \_ LAYER \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) es la misma que los PARÁMETROS DE CAPA [**D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), excepto que el miembro final de la estructura es ahora una [**enumeración D2D1 \_ LAYER \_ OPTIONS1.**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)</span><span class="sxs-lookup"><span data-stu-id="d9001-142">The [**D2D1\_LAYER\_PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) structure is the same as [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), except the final member of the structure is now a [**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) enumeration.</span></span>

<span data-ttu-id="d9001-143">[**D2D1 \_ LAYER \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) no tiene ninguna opción ClearType y tiene dos opciones diferentes que puede usar para mejorar el rendimiento:</span><span class="sxs-lookup"><span data-stu-id="d9001-143">[**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) has no ClearType option and has two different options that you can use to improve performance:</span></span>

-   <span data-ttu-id="d9001-144">[**D2D1 \_ LAYER \_ OPTIONS1 \_ INITIALIZE FROM \_ \_ BACKGROUND:**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)Direct2D representa primitivas en la capa sin borrarla con negro transparente.</span><span class="sxs-lookup"><span data-stu-id="d9001-144">[**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renders primitives to the layer without clearing it with transparent black.</span></span> <span data-ttu-id="d9001-145">Este no es el valor predeterminado, pero en la mayoría de los casos da como resultado un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d9001-145">This is not the default, but in most cases results in better performance.</span></span>

-   <span data-ttu-id="d9001-146">[**D2D1 \_ OPCIONES \_ DE CAPA1 \_ OMITIR \_ ALFA:**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)si la superficie subyacente está establecida en [**D2D1 \_ ALPHA MODE \_ \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), esta opción permite a Direct2D evitar modificar el canal alfa de la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-146">[**D2D1\_LAYER\_OPTIONS1\_IGNORE\_ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): if the underlying surface is set to [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), this option lets Direct2D avoid modifying the alpha channel of the layer.</span></span> <span data-ttu-id="d9001-147">No lo use en otros casos.</span><span class="sxs-lookup"><span data-stu-id="d9001-147">Do not use this in other cases.</span></span>

### <a name="blend-modes"></a><span data-ttu-id="d9001-148">Modos de fusión</span><span class="sxs-lookup"><span data-stu-id="d9001-148">Blend Modes</span></span>

<span data-ttu-id="d9001-149">A partir Windows 8, el contexto [](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) del dispositivo tiene un modo de combinación primitivo que determina cómo se combina cada primitivo con la superficie de destino.</span><span class="sxs-lookup"><span data-stu-id="d9001-149">Starting in Windows 8, the device context has a [**primitive blend mode**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) that determines how each primitive is blended with the target surface.</span></span> <span data-ttu-id="d9001-150">Este modo también se aplica a las capas cuando se llama al [**método PushLayer.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="d9001-150">This mode also applies to layers when you call the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span>

<span data-ttu-id="d9001-151">Por ejemplo, si usa una capa para recortar primitivas con transparencia, establezca el modo [**COPY \_ DE BLEND \_ \_ PRIMITIVO D2D1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) en el contexto del dispositivo para obtener los resultados adecuados.</span><span class="sxs-lookup"><span data-stu-id="d9001-151">For example, if you are using a layer to clip primitives with transparency set the [**D2D1\_PRIMITIVE\_BLEND\_COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) mode on the device context for proper results.</span></span> <span data-ttu-id="d9001-152">El modo de copia hace que el contexto del dispositivo interpola linealmente los 4 canales de color, incluido el canal alfa, de cada píxel con el contenido de la superficie de destino según la máscara geométrica de la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-152">The copy mode makes the device context linear interpolate all 4 color channels, including the alpha channel, of each pixel with the contents of the target surface according to the geometric mask of the layer.</span></span>

### <a name="interoperation"></a><span data-ttu-id="d9001-153">Interoperación</span><span class="sxs-lookup"><span data-stu-id="d9001-153">Interoperation</span></span>

<span data-ttu-id="d9001-154">A partir Windows 8, Direct2D admite la interoperación con Direct3D y GDI mientras se inserta una capa o un clip.</span><span class="sxs-lookup"><span data-stu-id="d9001-154">Starting in Windows 8, Direct2D supports interoperation with Direct3D and GDI while a layer or clip is pushed.</span></span> <span data-ttu-id="d9001-155">Se llama [**a ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) mientras se inserta una capa para interoperar con GDI.</span><span class="sxs-lookup"><span data-stu-id="d9001-155">You call [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) while a layer is pushed to interoperate with GDI.</span></span> <span data-ttu-id="d9001-156">Se llama [**a ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) y, a continuación, se representa en la superficie subyacente para interoperar con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d9001-156">You call [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) and then render to the underlying surface to interoperate with Direct3D.</span></span> <span data-ttu-id="d9001-157">Es su responsabilidad representar dentro de la capa o clip con Direct3D o GDI.</span><span class="sxs-lookup"><span data-stu-id="d9001-157">It is your responsibility to render inside the layer or clip with Direct3D or GDI.</span></span> <span data-ttu-id="d9001-158">Si intenta representar fuera de la capa o recortar los resultados no están definidos.</span><span class="sxs-lookup"><span data-stu-id="d9001-158">If you try to render outside the layer or clip the results are undefined.</span></span>

## <a name="creating-layers"></a><span data-ttu-id="d9001-159">Creación de capas</span><span class="sxs-lookup"><span data-stu-id="d9001-159">Creating Layers</span></span>

<span data-ttu-id="d9001-160">El trabajo con capas requiere estar familiarizado con los métodos [**CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))y [**PopLayer,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) y la estructura DE PARÁMETROS DE CAPA [**D2D1, \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) que contiene un conjunto de datos paramétricos que definen cómo se puede usar la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-160">Working with layers requires familiarity with the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) methods, and the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure, which contains a set of parametric data that defines how the layer can be used.</span></span> <span data-ttu-id="d9001-161">En la lista siguiente se describen los métodos y la estructura.</span><span class="sxs-lookup"><span data-stu-id="d9001-161">The following list describes the methods and structure.</span></span>

-   <span data-ttu-id="d9001-162">Llame al [**método CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para crear un recurso de capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-162">Call the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method to create a layer resource.</span></span>
    > [!Note]  
    > <span data-ttu-id="d9001-163">A partir Windows 8, puede omitir la llamada al método [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y, a continuación, pasar NULL al método [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) en la [**interfaz ID2D1DeviceContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)</span><span class="sxs-lookup"><span data-stu-id="d9001-163">Starting in Windows 8, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface.</span></span> <span data-ttu-id="d9001-164">Esto es más sencillo y permite que Direct2D administre automáticamente el recurso de capa y comparta recursos entre capas y gráficos de efectos.</span><span class="sxs-lookup"><span data-stu-id="d9001-164">This is simpler and allows Direct2D to automatically manage the layer resource and share resources between layers and effect graphs.</span></span>

     

-   <span data-ttu-id="d9001-165">Después de que el destino de representación haya empezado a dibujar (después de llamar a su [**método BeginDraw),**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) puede usar el [**método PushLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="d9001-165">After render target has begun drawing (after its [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method has been called), you can use the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="d9001-166">El **método PushLayer** agrega la capa especificada al destino de representación, de modo que el destino recibe todas las operaciones de dibujo posteriores hasta que se llama a [**PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)</span><span class="sxs-lookup"><span data-stu-id="d9001-166">The **PushLayer** method adds the specified layer to the render target, so that the target receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <span data-ttu-id="d9001-167">Este método toma un [**objeto ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) devuelto llamando a [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) y *a layerParameters* en la estructura DE PARÁMETROS [**DE \_ CAPA \_ D2D1.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)</span><span class="sxs-lookup"><span data-stu-id="d9001-167">This method takes an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) object returned by calling [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) and an *layerParameters* in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure.</span></span> <span data-ttu-id="d9001-168">En la tabla siguiente se describen los campos de la estructura .</span><span class="sxs-lookup"><span data-stu-id="d9001-168">The following table describes the fields of the structure.</span></span> 

    | <span data-ttu-id="d9001-169">Campo</span><span class="sxs-lookup"><span data-stu-id="d9001-169">Field</span></span>                 | <span data-ttu-id="d9001-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9001-170">Description</span></span>|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d9001-171">**contentBounds**</span><span class="sxs-lookup"><span data-stu-id="d9001-171">**contentBounds**</span></span>     | <span data-ttu-id="d9001-172">Límites de contenido de la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-172">The content bounds of the layer.</span></span> <span data-ttu-id="d9001-173">El contenido no se representará fuera de estos límites.</span><span class="sxs-lookup"><span data-stu-id="d9001-173">Content won't render outside these bounds.</span></span> <span data-ttu-id="d9001-174">Este parámetro tiene como valor predeterminado [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span><span class="sxs-lookup"><span data-stu-id="d9001-174">This parameter defaults to [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span></span> <span data-ttu-id="d9001-175">Cuando se usa el valor predeterminado, los límites de contenido se toman eficazmente como límites del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="d9001-175">When the default value is used, the content bounds are effectively taken to be the bounds of the render target.</span></span> |
    | <span data-ttu-id="d9001-176">**geometricMask**</span><span class="sxs-lookup"><span data-stu-id="d9001-176">**geometricMask**</span></span>     | <span data-ttu-id="d9001-177">(Opcional) Área, definida por [**id2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)al que se debe recortar la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-177">(Optional) The area, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), to which the layer should be clipped.</span></span> <span data-ttu-id="d9001-178">Establezca en **NULL** si la capa no se debe recortar a una geometría.</span><span class="sxs-lookup"><span data-stu-id="d9001-178">Set to **NULL** if the layer shouldn't be clipped to a geometry.</span></span> |
    | <span data-ttu-id="d9001-179">**maskAntialiasMode**</span><span class="sxs-lookup"><span data-stu-id="d9001-179">**maskAntialiasMode**</span></span> | <span data-ttu-id="d9001-180">Valor que especifica el modo de suavizado de contorno para la máscara geométrica especificada por el **campo geometricMask.**</span><span class="sxs-lookup"><span data-stu-id="d9001-180">A value that specifies the antialiasing mode for the geometric mask specified by the **geometricMask** field.</span></span> |
    | <span data-ttu-id="d9001-181">**maskTransform**</span><span class="sxs-lookup"><span data-stu-id="d9001-181">**maskTransform**</span></span>     | <span data-ttu-id="d9001-182">Valor que especifica la transformación que se aplica a la máscara geométrica al componer la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-182">A value that specifies the transform that is applied to the geometric mask when composing the layer.</span></span> <span data-ttu-id="d9001-183">Esto es relativo a la transformación del mundo.</span><span class="sxs-lookup"><span data-stu-id="d9001-183">This is relative to the world transform.</span></span>  |
    | <span data-ttu-id="d9001-184">**Opacidad**</span><span class="sxs-lookup"><span data-stu-id="d9001-184">**opacity**</span></span>           | <span data-ttu-id="d9001-185">Valor de opacidad de la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-185">The opacity value of the layer.</span></span> <span data-ttu-id="d9001-186">La opacidad de cada recurso de la capa se multiplica con este valor al componer en el destino.</span><span class="sxs-lookup"><span data-stu-id="d9001-186">The opacity of each resource in the layer is multiplied with this value when compositing to the target.</span></span>  |
    | <span data-ttu-id="d9001-187">**opacityBrush**</span><span class="sxs-lookup"><span data-stu-id="d9001-187">**opacityBrush**</span></span>      | <span data-ttu-id="d9001-188">(Opcional) Pincel que se usa para modificar la opacidad de la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-188">(Optional) A brush that is used to modify the opacity of the layer.</span></span> <span data-ttu-id="d9001-189">El pincel se asigna a la capa y el canal alfa de cada píxel de pincel asignado se multiplica con respecto al píxel de capa correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d9001-189">The brush is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.</span></span> <span data-ttu-id="d9001-190">Establezca en **NULL** si la capa no debe tener una máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="d9001-190">Set to **NULL** if the layer shouldn't have an opacity mask.</span></span>   |
    | <span data-ttu-id="d9001-191">**layerOptions**</span><span class="sxs-lookup"><span data-stu-id="d9001-191">**layerOptions**</span></span>      | <span data-ttu-id="d9001-192">Valor que especifica si la capa pretende representar texto con suavizado de contorno ClearType.</span><span class="sxs-lookup"><span data-stu-id="d9001-192">A value that specifies whether the layer intends to render text with ClearType antialiasing.</span></span> <span data-ttu-id="d9001-193">El valor predeterminado de este parámetro es off.</span><span class="sxs-lookup"><span data-stu-id="d9001-193">This parameter defaults to off.</span></span> <span data-ttu-id="d9001-194">Activarlo permite que ClearType funcione correctamente, pero da como resultado una velocidad de representación ligeramente más lenta.</span><span class="sxs-lookup"><span data-stu-id="d9001-194">Turning it on enables ClearType to work correctly, but it results in slightly slower rendering speed.</span></span>    |

    

     

    > [!Note]  
    > <span data-ttu-id="d9001-195">A partir Windows 8, no se puede representar con ClearType en una capa, por lo que el parámetro **layerOptions** siempre debe establecerse en [**D2D1 \_ LAYER OPTIONS \_ \_ NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span><span class="sxs-lookup"><span data-stu-id="d9001-195">Starting in Windows 8, you cannot render with ClearType in a layer, so the **layerOptions** parameter should always be set to [**D2D1\_LAYER\_OPTIONS\_NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span></span>

     

    <span data-ttu-id="d9001-196">Para mayor comodidad, Direct2D proporciona el método [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) para ayudarle a crear estructuras [**de PARÁMETROS DE CAPA D2D1. \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)</span><span class="sxs-lookup"><span data-stu-id="d9001-196">For convenience, Direct2D provides the [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) method to help you create [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structures.</span></span>

-   <span data-ttu-id="d9001-197">Para componer el contenido de la capa en el destino de representación, llame al [**método PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)</span><span class="sxs-lookup"><span data-stu-id="d9001-197">To composite the contents of the layer into the render target, call the [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) method.</span></span> <span data-ttu-id="d9001-198">Debe llamar al método **PopLayer** antes de llamar al [**método EndDraw.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)</span><span class="sxs-lookup"><span data-stu-id="d9001-198">You must call the **PopLayer** method before you call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span>

<span data-ttu-id="d9001-199">En el ejemplo siguiente se muestra cómo usar [**CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))y [**PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)</span><span class="sxs-lookup"><span data-stu-id="d9001-199">The following example shows how to use [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span></span> <span data-ttu-id="d9001-200">Todos los campos de la estructura DE PARÁMETROS DE CAPA [**\_ \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) se establecen en sus valores predeterminados, excepto **opacityBrush**, que se establece en [**id2D1RadialGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)</span><span class="sxs-lookup"><span data-stu-id="d9001-200">All fields in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to their defaults, except **opacityBrush**, which is set to an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>


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



<span data-ttu-id="d9001-201">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d9001-201">Code has been omitted from this example.</span></span>

<span data-ttu-id="d9001-202">Tenga en cuenta que cuando llame a [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) y [**PopLayer,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)asegúrese de que **cada PushLayer** tiene una llamada **a PopLayer correspondiente.**</span><span class="sxs-lookup"><span data-stu-id="d9001-202">Note that when you call [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ensure that each **PushLayer** has a matching **PopLayer** call.</span></span> <span data-ttu-id="d9001-203">Si hay más llamadas **a PopLayer** que llamadas **pushLayer,** el destino de representación se coloca en un estado de error.</span><span class="sxs-lookup"><span data-stu-id="d9001-203">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="d9001-204">Si se llama a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) antes de que se coloquen todas las capas pendientes, el destino de representación se coloca en un estado de error y devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d9001-204">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state and returns an error.</span></span> <span data-ttu-id="d9001-205">Para borrar el estado de error, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="d9001-205">To clear the error state, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

## <a name="content-bounds"></a><span data-ttu-id="d9001-206">Límites de contenido</span><span class="sxs-lookup"><span data-stu-id="d9001-206">Content Bounds</span></span>

<span data-ttu-id="d9001-207">**ContentBounds establece** el límite de lo que se va a dibujar en la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-207">The **contentBounds** sets the limit of what is to be drawn to the layer.</span></span> <span data-ttu-id="d9001-208">Solo los elementos dentro de los límites de contenido se componen de nuevo en el destino de representación.</span><span class="sxs-lookup"><span data-stu-id="d9001-208">Only those things within the content bounds are composited back to the render target.</span></span>

<span data-ttu-id="d9001-209">En el ejemplo siguiente se muestra cómo especificar **contentBounds** para que la imagen original se recorte a los límites de contenido con la esquina superior izquierda en (10, 108) y la esquina inferior derecha en (121, 177).</span><span class="sxs-lookup"><span data-stu-id="d9001-209">The example that follows shows how to specify **contentBounds** so that the original image is clipped to the content bounds with the upper-left corner at (10, 108) and the lower-right corner at (121, 177).</span></span> <span data-ttu-id="d9001-210">En la ilustración siguiente se muestra la imagen original y el resultado de recortar la imagen a los límites de contenido.</span><span class="sxs-lookup"><span data-stu-id="d9001-210">The following illustration shows the original image and the result of clipping the image to the content bounds.</span></span>

![ilustración de límites de contenido en una imagen original y la imagen recortada resultante](images/layers-contentbounds.png)


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



<span data-ttu-id="d9001-212">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d9001-212">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="d9001-213">La imagen recortada resultante se ve afectada aún más si se especifica **una geometríaMask**.</span><span class="sxs-lookup"><span data-stu-id="d9001-213">The resulting clipped image is further affected if you specify a **geometricMask**.</span></span> <span data-ttu-id="d9001-214">Consulte la [sección Máscaras geométricas](#geometric-masks) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="d9001-214">See the [Geometric Masks](#geometric-masks) section for more information.</span></span>

 

## <a name="geometric-masks"></a><span data-ttu-id="d9001-215">Máscaras geométricas</span><span class="sxs-lookup"><span data-stu-id="d9001-215">Geometric Masks</span></span>

<span data-ttu-id="d9001-216">Una máscara geométrica es un clip o un recorte, definido por un objeto [**ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) que enmascara una capa cuando se dibuja mediante un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="d9001-216">A geometric mask is a clip or a cutout, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="d9001-217">Puede usar el campo **geometryMask de** la estructura DE PARÁMETROS [**DE \_ CAPA \_ D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) para enmascarar los resultados en una geometría.</span><span class="sxs-lookup"><span data-stu-id="d9001-217">You can use the **geometricMask** field of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to mask the results to a geometry.</span></span> <span data-ttu-id="d9001-218">Por ejemplo, si desea mostrar una imagen enmascarada por una letra de bloque "A", primero puede crear una geometría que represente la letra de bloque "A" y usar esa geometría como máscara geométrica para una capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-218">For example, if you want to display an image masked by a block letter "A", you can first create a geometry representing the block letter "A" and use that geometry as a geometric mask for a layer.</span></span> <span data-ttu-id="d9001-219">Después de insertar la capa, puede dibujar la imagen.</span><span class="sxs-lookup"><span data-stu-id="d9001-219">Then, after pushing the layer, you can draw the image.</span></span> <span data-ttu-id="d9001-220">Al hacer clic en la capa, la imagen se recorta a la forma "A" de la letra de bloque.</span><span class="sxs-lookup"><span data-stu-id="d9001-220">Popping the layer results in the image being clipped to the block letter "A" shape.</span></span>

<span data-ttu-id="d9001-221">En el ejemplo siguiente se muestra cómo crear un [**id2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) que contiene una forma de una montaña y, a continuación, pasar la geometría de ruta de acceso a [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="d9001-221">The example that follows shows how to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) containing a shape of a mountain and then pass the path geometry to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span></span> <span data-ttu-id="d9001-222">A continuación, dibuja un mapa de bits y cuadrados.</span><span class="sxs-lookup"><span data-stu-id="d9001-222">It then draws a bitmap and squares.</span></span> <span data-ttu-id="d9001-223">Si solo hay un mapa de bits en la capa que se va a representar, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de mapa de bits con fijación para mejorar la eficacia.</span><span class="sxs-lookup"><span data-stu-id="d9001-223">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="d9001-224">En la siguiente ilustración se muestra el resultado del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d9001-224">The following illustration shows the output from the example.</span></span>

![ilustración de una imagen de una hoja y la imagen resultante después de aplicar una máscara geométrica de una montaña](images/layers-bitmapmask.png)

<span data-ttu-id="d9001-226">En el primer ejemplo se define la geometría que se va a usar como máscara.</span><span class="sxs-lookup"><span data-stu-id="d9001-226">The first example defines the geometry to be used as a mask.</span></span>


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



<span data-ttu-id="d9001-227">En el ejemplo siguiente se usa la geometría como máscara para la capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-227">The next example uses the geometry as a mask for the layer.</span></span>


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



<span data-ttu-id="d9001-228">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d9001-228">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="d9001-229">En general, si especifica una **geometríaMask**, puede usar el valor predeterminado, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), para **contentBounds**.</span><span class="sxs-lookup"><span data-stu-id="d9001-229">In general, if you specify a **geometricMask**, you can use the default value, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), for the **contentBounds**.</span></span>
>
> <span data-ttu-id="d9001-230">Si **contentBounds** es NULL y **geometricMask** no es NULL, los límites de contenido son efectivamente los límites de la máscara geométrica después de aplicar la transformación de máscara.</span><span class="sxs-lookup"><span data-stu-id="d9001-230">If **contentBounds** is NULL, and **geometricMask** is non-NULL, then the content bounds are effectively the bounds of the geometric mask after the mask transform is applied.</span></span>
>
> <span data-ttu-id="d9001-231">Si **contentBounds** no es NULL y **geometricMask** no es NULL, la máscara geométrica transformada se recorta eficazmente en los límites de contenido y se supone que los límites de contenido son infinitos.</span><span class="sxs-lookup"><span data-stu-id="d9001-231">If **contentBounds** is non-NULL, and **geometricMask** is non-NULL, then the transformed geometric mask is effectively clipped against content bounds and the content bounds are assumed to be infinite.</span></span>

 

## <a name="opacity-masks"></a><span data-ttu-id="d9001-232">Máscaras de opacidad</span><span class="sxs-lookup"><span data-stu-id="d9001-232">Opacity Masks</span></span>

<span data-ttu-id="d9001-233">Una máscara de opacidad es una máscara, descrita por un pincel o mapa de bits, que se aplica a otro objeto para que ese objeto sea parcial o completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="d9001-233">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="d9001-234">Permite usar el canal alfa de un pincel como máscara de contenido.</span><span class="sxs-lookup"><span data-stu-id="d9001-234">It allows the use of the alpha channel of a brush to be used as a content mask.</span></span> <span data-ttu-id="d9001-235">Por ejemplo, puede definir un pincel de degradado radial que varíe de opaco a transparente para crear un efecto de viñeta.</span><span class="sxs-lookup"><span data-stu-id="d9001-235">For example, you can define a radial gradient brush that varies from opaque to transparent to create a vignette effect.</span></span>

<span data-ttu-id="d9001-236">En el ejemplo siguiente se usa [**id2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) como máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="d9001-236">The example that follows uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m\_pRadialGradientBrush*) as an opacity mask.</span></span> <span data-ttu-id="d9001-237">A continuación, dibuja un mapa de bits y cuadrados.</span><span class="sxs-lookup"><span data-stu-id="d9001-237">It then draws a bitmap and squares.</span></span> <span data-ttu-id="d9001-238">Si solo hay un mapa de bits en la capa que se va a representar, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de mapa de bits con fijación para mejorar la eficacia.</span><span class="sxs-lookup"><span data-stu-id="d9001-238">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="d9001-239">En la ilustración siguiente se muestra la salida de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d9001-239">The following illustration shows the output from this example.</span></span>

![ilustración de una imagen de árboles y la imagen resultante después de aplicar una máscara de opacidad](images/layers-opacitymask.png)


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



<span data-ttu-id="d9001-241">El código se ha omitido en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d9001-241">Code has been omitted from this example.</span></span>

> [!Note]  
> <span data-ttu-id="d9001-242">En este ejemplo se usa una capa para aplicar una máscara de opacidad a un solo objeto para que el ejemplo sea lo más sencillo posible.</span><span class="sxs-lookup"><span data-stu-id="d9001-242">This example uses a layer to apply an opacity mask to a single object to keep the example as simple as possible.</span></span> <span data-ttu-id="d9001-243">Al aplicar una máscara de opacidad a un solo objeto, es más eficaz usar los métodos [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) o [**FillGeometry,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) en lugar de una capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-243">When applying an opacity mask to a single object, its more efficient to use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) or [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods, rather than a layer.</span></span>

 

<span data-ttu-id="d9001-244">Para obtener instrucciones sobre cómo aplicar una máscara de opacidad sin usar una capa, vea La información general [sobre las máscaras de opacidad](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d9001-244">For instructions on how to apply an opacity mask without using a layer, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="alternatives-to-layers"></a><span data-ttu-id="d9001-245">Alternativas a las capas</span><span class="sxs-lookup"><span data-stu-id="d9001-245">Alternatives to Layers</span></span>

<span data-ttu-id="d9001-246">Como se mencionó anteriormente, un número excesivo de capas puede afectar negativamente al rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d9001-246">As mentioned earlier, excessive number of layers can adversely affect the performance of your application.</span></span> <span data-ttu-id="d9001-247">Para mejorar el rendimiento, evite usar capas siempre que sea posible; en su lugar, use sus alternativas.</span><span class="sxs-lookup"><span data-stu-id="d9001-247">To improve performance, avoid using layers whenever possible; instead use their alternatives.</span></span> <span data-ttu-id="d9001-248">En el ejemplo de código siguiente se muestra cómo usar [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) y [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) para recortar una región, como alternativa al uso de una capa con límites de contenido.</span><span class="sxs-lookup"><span data-stu-id="d9001-248">The following code example shows how to use [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to clip a region, as an alternative to using a layer with content bounds.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



<span data-ttu-id="d9001-249">De forma similar, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de mapa de bits con fijación como alternativa al uso de una capa con una máscara de opacidad cuando solo hay un contenido en la capa que se va a representar, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d9001-249">Similarly, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush as an alternative to using a layer with an opacity mask when there is only one content in the layer to render, as shown in the following example.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



<span data-ttu-id="d9001-250">Como alternativa al uso de una capa con una máscara geométrica, considere la posibilidad de usar una máscara de mapa de bits para recortar una región, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d9001-250">As an alternative to using a layer with a geometric mask, consider using a bitmap mask to clip a region, as shown in the following example.</span></span>


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



<span data-ttu-id="d9001-251">Por último, si desea aplicar opacidad a una sola primitiva, debe multiplicar la opacidad en en el color del pincel y, a continuación, representar la primitiva.</span><span class="sxs-lookup"><span data-stu-id="d9001-251">Lastly, if you want to apply opacity to a single primitive, you should multiply the opacity into the into the brush color and then render the primitive.</span></span> <span data-ttu-id="d9001-252">No necesita una capa ni un mapa de bits de máscara de opacidad.</span><span class="sxs-lookup"><span data-stu-id="d9001-252">You do not need a layer or an opacity mask bitmap.</span></span>


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



## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="d9001-253">Recorte de una forma arbitraria</span><span class="sxs-lookup"><span data-stu-id="d9001-253">Clipping an arbitrary shape</span></span>

<span data-ttu-id="d9001-254">En la ilustración siguiente se muestra el resultado de aplicar un clip a una imagen.</span><span class="sxs-lookup"><span data-stu-id="d9001-254">The figure here shows the result of applying a clip to an image.</span></span>

![una imagen que muestra un ejemplo de una imagen antes y después de un clip.](images/clip.png)

<span data-ttu-id="d9001-256">Puede obtener este resultado mediante capas con una máscara de geometría o el [**método FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) con un pincel de opacidad.</span><span class="sxs-lookup"><span data-stu-id="d9001-256">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="d9001-257">Este es un ejemplo que usa una capa:</span><span class="sxs-lookup"><span data-stu-id="d9001-257">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="d9001-258">Este es un ejemplo que usa el [**método FillGeometry:**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)</span><span class="sxs-lookup"><span data-stu-id="d9001-258">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


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



<span data-ttu-id="d9001-259">En este ejemplo de código, cuando se llama al método PushLayer, no se pasa una capa creada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d9001-259">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="d9001-260">Direct2D crea una capa automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d9001-260">Direct2D creates a layer for you.</span></span> <span data-ttu-id="d9001-261">Direct2D puede administrar la asignación y destrucción de este recurso sin intervención de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d9001-261">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="d9001-262">Esto permite a Direct2D reutilizar capas internamente y aplicar optimizaciones de administración de recursos.</span><span class="sxs-lookup"><span data-stu-id="d9001-262">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

> [!Note]  
> <span data-ttu-id="d9001-263">En Windows 8 se han realizado muchas optimizaciones para el uso de capas y se recomienda intentar usar las API de capa en lugar de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="d9001-263">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

 

### <a name="axis-aligned-clips"></a><span data-ttu-id="d9001-264">Clips alineados en el eje</span><span class="sxs-lookup"><span data-stu-id="d9001-264">Axis aligned clips</span></span>

<span data-ttu-id="d9001-265">Si la región que se va a recortar está alineada con el eje de la superficie de dibujo, en lugar de arbitraria.</span><span class="sxs-lookup"><span data-stu-id="d9001-265">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="d9001-266">Este caso es adecuado para usar un rectángulo de recorte en lugar de una capa.</span><span class="sxs-lookup"><span data-stu-id="d9001-266">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="d9001-267">La ganancia de rendimiento es más para la geometría con alias que para la geometría suavizada.</span><span class="sxs-lookup"><span data-stu-id="d9001-267">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="d9001-268">Para obtener más información sobre los clips alineados con el eje, vea el [**tema PushAxisAlignedClip.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="d9001-268">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9001-269">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9001-269">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9001-270">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="d9001-270">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 