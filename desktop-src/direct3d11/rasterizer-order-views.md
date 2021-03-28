---
title: Vistas de orden de rasterizador
description: Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de UAV con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs.
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149494"
---
# <a name="rasterizer-order-views"></a><span data-ttu-id="669b0-103">Vistas de orden de rasterizador</span><span class="sxs-lookup"><span data-stu-id="669b0-103">Rasterizer Order Views</span></span>

<span data-ttu-id="669b0-104">Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de UAV con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs.</span><span class="sxs-lookup"><span data-stu-id="669b0-104">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span> <span data-ttu-id="669b0-105">Esto permite que funcionen los algoritmos de transparencia independiente de orden (OIT), que proporcionan resultados de representación mucho mejores cuando varios objetos transparentes están alineados entre sí en una vista.</span><span class="sxs-lookup"><span data-stu-id="669b0-105">This enables Order Independent Transparency (OIT) algorithms to work, which give much better rendering results when multiple transparent objects are in line with each other in a view.</span></span>

-   [<span data-ttu-id="669b0-106">Información general</span><span class="sxs-lookup"><span data-stu-id="669b0-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="669b0-107">Detalles de implementación</span><span class="sxs-lookup"><span data-stu-id="669b0-107">Implementation details</span></span>](#implementation-details)
-   [<span data-ttu-id="669b0-108">Resumen de API</span><span class="sxs-lookup"><span data-stu-id="669b0-108">API summary</span></span>](#api-summary)
-   [<span data-ttu-id="669b0-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="669b0-109">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="669b0-110">Información general</span><span class="sxs-lookup"><span data-stu-id="669b0-110">Overview</span></span>

<span data-ttu-id="669b0-111">Las canalizaciones de gráficos estándar pueden tener problemas al componer varias texturas que contienen transparencias correctamente.</span><span class="sxs-lookup"><span data-stu-id="669b0-111">Standard graphics pipelines may have trouble correctly compositing together multiple textures that contain transparency.</span></span> <span data-ttu-id="669b0-112">Los objetos como las barreras de alambres, humos, incendios, vegetación y vidrio en color usan transparencia para obtener el efecto deseado.</span><span class="sxs-lookup"><span data-stu-id="669b0-112">Objects such as wire fences, smoke, fire, vegetation, and colored glass use transparency to get the desired effect.</span></span> <span data-ttu-id="669b0-113">Surgen problemas cuando varias texturas que contienen transparencias están alineadas entre sí (humo delante de una barrera delante de un edificio de vidrio que contiene vegetación, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="669b0-113">Problems arise when multiple textures that contain transparency are in line with each other (smoke in front of a fence in front of a glass building containing vegetation, as an example).</span></span> <span data-ttu-id="669b0-114">Las vistas ordenadas de rasterizador (ROVs) permiten que los algoritmos OIT subyacentes usen características del hardware para intentar resolver el orden de transparencia correctamente.</span><span class="sxs-lookup"><span data-stu-id="669b0-114">Rasterizer ordered views (ROVs) enable the underlying OIT algorithms to use features of the hardware to try to resolve the transparency order correctly.</span></span> <span data-ttu-id="669b0-115">El sombreador de píxeles controla la transparencia.</span><span class="sxs-lookup"><span data-stu-id="669b0-115">Transparency is handled by the pixel shader.</span></span>

<span data-ttu-id="669b0-116">Las vistas ordenadas de rasterizador (ROVs) permiten que el código del sombreador de píxeles marque los enlaces de UAV con una declaración que modifica los requisitos normales para el orden de los resultados de la canalización de gráficos para UAVs.</span><span class="sxs-lookup"><span data-stu-id="669b0-116">Rasterizer ordered views (ROVs) allow pixel shader code to mark UAV bindings with a declaration that alters the normal requirements for the order of graphics pipeline results for UAVs.</span></span>

<span data-ttu-id="669b0-117">ROVs garantiza el orden de los accesos a UAV para cualquier par de invocaciones del sombreador de píxeles superpuestos.</span><span class="sxs-lookup"><span data-stu-id="669b0-117">ROVs guarantee the order of UAV accesses for any pair of overlapping pixel shader invocations.</span></span> <span data-ttu-id="669b0-118">En este caso "superpuesta" significa que las invocaciones se generan mediante las mismas llamadas a Draw y comparten la misma coordenada de píxeles en el modo de ejecución de frecuencia de píxeles y el mismo píxel y la coordenada de ejemplo en el modo de frecuencia de muestreo.</span><span class="sxs-lookup"><span data-stu-id="669b0-118">In this case “overlapping” means that the invocations are generated by the same draw calls and share the same pixel coordinate when in pixel-frequency execution mode, and the same pixel and sample coordinate in sample-frequency mode.</span></span>

<span data-ttu-id="669b0-119">El orden en que se ejecutan los accesos ROV superpuestos de las invocaciones del sombreador de píxeles es idéntico al orden en el que se envía la geometría.</span><span class="sxs-lookup"><span data-stu-id="669b0-119">The order in which overlapping ROV accesses of pixel shader invocations are executed is identical to the order in which the geometry is submitted.</span></span> <span data-ttu-id="669b0-120">Esto significa que, para las invocaciones del sombreador de píxeles superpuestos, las escrituras de ROV realizadas por una invocación del sombreador de píxeles deben estar disponibles para ser leídas por una invocación posterior y no deben afectar a las lecturas realizadas por una invocación anterior.</span><span class="sxs-lookup"><span data-stu-id="669b0-120">This means that, for overlapping pixel shader invocations, ROV writes performed by a pixel shader invocation must be available to be read by a subsequent invocation and must not affect reads by a previous invocation.</span></span> <span data-ttu-id="669b0-121">Las lecturas de ROV realizadas por una invocación del sombreador de píxeles deben reflejar las escrituras realizadas por una invocación anterior y no deben reflejar las escrituras en una invocación posterior.</span><span class="sxs-lookup"><span data-stu-id="669b0-121">ROV reads performed by a pixel shader invocation must reflect writes by a previous invocation and must not reflect writes by a subsequent invocation.</span></span> <span data-ttu-id="669b0-122">Esto es importante para UAVs porque se omiten explícitamente en las garantías de invarianza de salida establecidas normalmente por el orden fijo de los resultados de la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="669b0-122">This is important for UAVs because they are explicitly omitted from the output-invariance guarantees normally set by the fixed order of graphics pipeline results.</span></span>

## <a name="implementation-details"></a><span data-ttu-id="669b0-123">Detalles de la implementación</span><span class="sxs-lookup"><span data-stu-id="669b0-123">Implementation details</span></span>

<span data-ttu-id="669b0-124">Las vistas ordenadas de rasterizador (ROVs) se declaran con los siguientes objetos del lenguaje HLSL (High Level Shader Language) y solo están disponibles para el sombreador de píxeles:</span><span class="sxs-lookup"><span data-stu-id="669b0-124">Rasterizer ordered views (ROVs) are declared with the following new High Level Shader Language (HLSL) objects, and are only available to the pixel shader:</span></span>

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

<span data-ttu-id="669b0-125">Utilice estos objetos de la misma manera que otros objetos UAV (como, por ejemplo, `RWBuffer` etc.).</span><span class="sxs-lookup"><span data-stu-id="669b0-125">Use these objects in the same manner as other UAV objects (such as `RWBuffer` etc.).</span></span>

## <a name="api-summary"></a><span data-ttu-id="669b0-126">API summary</span><span class="sxs-lookup"><span data-stu-id="669b0-126">API summary</span></span>

<span data-ttu-id="669b0-127">ROVs son una construcción solo HLSL que aplica una semántica de comportamiento diferente a UAVs.</span><span class="sxs-lookup"><span data-stu-id="669b0-127">ROVs are an HLSL-only construct that applies different behavior semantics to UAVs.</span></span> <span data-ttu-id="669b0-128">Todas las API relevantes para UAVs también son relevantes para ROVs.</span><span class="sxs-lookup"><span data-stu-id="669b0-128">All APIs relevant to UAVs are also relevant to ROVs.</span></span> <span data-ttu-id="669b0-129">Tenga en cuenta que el siguiente método, las estructuras y la clase auxiliar hacen referencia al rasterizador:</span><span class="sxs-lookup"><span data-stu-id="669b0-129">Note that the following method, structures, and helper class reference the rasterizer:</span></span>

-   <span data-ttu-id="669b0-130">[**D3D11 \_ RASTERIZAdor \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : estructura que contiene la descripción del rasterizador, anotando la \_ \_ clase auxiliar CD3D12 de rasterizador DESC2 para crear descripciones de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="669b0-130">[**D3D11\_RASTERIZER\_DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : structure holding the rasterizer description, noting the CD3D12\_RASTERIZER\_DESC2 helper class for creating rasterizer descriptions.</span></span>
-   <span data-ttu-id="669b0-131">[**D3D11 \_ \_Data Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : estructura que contiene el valor booleano `ROVsSupported` , que indica la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="669b0-131">[**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : structure holding the boolean `ROVsSupported`, indicating the support.</span></span>
-   <span data-ttu-id="669b0-132">[**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : método para tener acceso a las características admitidas.</span><span class="sxs-lookup"><span data-stu-id="669b0-132">[**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : method to access the supported features.</span></span>

## <a name="related-topics"></a><span data-ttu-id="669b0-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="669b0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="669b0-134">Características de Direct3D 11,3</span><span class="sxs-lookup"><span data-stu-id="669b0-134">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="669b0-135">Modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="669b0-135">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 