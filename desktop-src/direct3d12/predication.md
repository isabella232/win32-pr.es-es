---
title: Predication
description: Predication es una característica que permite que la GPU en lugar de la CPU determine no dibujar, copiar o enviar un objeto.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2020
ms.locfileid: "104549157"
---
# <a name="predication"></a><span data-ttu-id="d05f7-103">Predication</span><span class="sxs-lookup"><span data-stu-id="d05f7-103">Predication</span></span>

<span data-ttu-id="d05f7-104">Predication es una característica que permite que la GPU en lugar de la CPU determine no dibujar, copiar o enviar un objeto.</span><span class="sxs-lookup"><span data-stu-id="d05f7-104">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy, or dispatch an object.</span></span>

-   [<span data-ttu-id="d05f7-105">Información general</span><span class="sxs-lookup"><span data-stu-id="d05f7-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="d05f7-106">SetPredication</span><span class="sxs-lookup"><span data-stu-id="d05f7-106">SetPredication</span></span>](#setpredication)
-   [<span data-ttu-id="d05f7-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d05f7-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="d05f7-108">Información general</span><span class="sxs-lookup"><span data-stu-id="d05f7-108">Overview</span></span>

<span data-ttu-id="d05f7-109">El uso típico de predication es con oclusión; Si se dibuja un cuadro de límite y es ocluidos, obviamente no hay ningún punto en el dibujo del propio objeto.</span><span class="sxs-lookup"><span data-stu-id="d05f7-109">The typical use of predication is with occlusion; if a bounding box is drawn and is occluded, there is obviously no point in drawing the object itself.</span></span> <span data-ttu-id="d05f7-110">En esta situación, se puede "predicar" el dibujo del objeto, lo que permite su eliminación de la representación real por parte de la GPU.</span><span class="sxs-lookup"><span data-stu-id="d05f7-110">In this situation, the drawing of the object can be "predicated", enabling its removal from actual rendering by the GPU.</span></span>

<span data-ttu-id="d05f7-111">En primer lugar, esto podría parecer redudant y por encima de la prueba de profundidad estándar más un paso de profundidad temprana.</span><span class="sxs-lookup"><span data-stu-id="d05f7-111">At first, this might seem redudant over and above the standard depth test plus an early depth pass.</span></span> <span data-ttu-id="d05f7-112">Sin embargo, predication puede quitar la sobrecarga del estado del comando Draw en sí, además de la rasterización.</span><span class="sxs-lookup"><span data-stu-id="d05f7-112">But predication can remove the overhead of the draw command state itself, plus the rasterization.</span></span> <span data-ttu-id="d05f7-113">Aunque una fase de profundidad temprana quita los píxeles innecesarios, todavía puede ejecutar sombreadores de vértices, de casco, de dominio y de geometría, e invocar el ensamblador de entrada de función fija, tesselator y rasterizador.</span><span class="sxs-lookup"><span data-stu-id="d05f7-113">While an early depth pass removes unnecessary pixels, it can still execute vertex, hull, domain, and geometry shaders, and invoke the fixed-function input assembler, tesselator, and rasterizer.</span></span> <span data-ttu-id="d05f7-114">Al dibujar un rectángulo de selección simple o un volumen de límite similar &mdash; que sea más fácil de procesar y Rasterizar que el modelo real &mdash; , se evita la rasterización y el procesamiento innecesarios.</span><span class="sxs-lookup"><span data-stu-id="d05f7-114">By drawing a simple bounding box or similar bounding volume&mdash;which is simpler to process and rasterize than the real model&mdash;you avoid unnecessary rasterization and processing.</span></span>

<span data-ttu-id="d05f7-115">A diferencia de Direct3D 11, predication está desacoplado de las consultas y se expande en Direct3D 12 para permitir que una aplicación Predicate objetos en función de la razón por la que el desarrollador de la aplicación puede decidir (no solo oclusión).</span><span class="sxs-lookup"><span data-stu-id="d05f7-115">Unlike Direct3D 11, predication is decoupled from queries, and is expanded in Direct3D 12 to enable an application to predicate objects based on any reasoning the app developer may decide on (not just occlusion).</span></span>

## <a name="setpredication"></a><span data-ttu-id="d05f7-116">SetPredication</span><span class="sxs-lookup"><span data-stu-id="d05f7-116">SetPredication</span></span>

<span data-ttu-id="d05f7-117">Predication se puede establecer en función del valor de 64 bits dentro de un búfer (consulte [**D3D12 \_ Predication \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span><span class="sxs-lookup"><span data-stu-id="d05f7-117">Predication can be set based on the value of 64-bits within a buffer (refer to [**D3D12\_PREDICATION\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).</span></span>

<span data-ttu-id="d05f7-118">Cuando la GPU ejecuta un comando [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , ajusta el valor en el búfer.</span><span class="sxs-lookup"><span data-stu-id="d05f7-118">When the GPU executes a [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) command it snaps the value in the buffer.</span></span> <span data-ttu-id="d05f7-119">Los cambios futuros en los datos del búfer no afectan al estado predication.</span><span class="sxs-lookup"><span data-stu-id="d05f7-119">Future changes to the data in the buffer do not retroactively affect the predication state.</span></span>

<span data-ttu-id="d05f7-120">Si el búfer de parámetros de entrada es NULL, predication está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d05f7-120">If the input parameter Buffer is NULL, then predication is disabled.</span></span>

<span data-ttu-id="d05f7-121">Las sugerencias de Predication no están presentes en la API de Direct3D 12. y predication se permiten en las listas de comandos Direct, Compute y Copy.</span><span class="sxs-lookup"><span data-stu-id="d05f7-121">Predication hints are not present in the Direct3D 12 API; and predication is allowed on direct, compute, and copy command lists.</span></span> <span data-ttu-id="d05f7-122">El búfer de origen puede estar en cualquier tipo de montón (valor predeterminado, cargar, readback, personalizado).</span><span class="sxs-lookup"><span data-stu-id="d05f7-122">The source buffer can be in any heap type (default, upload, readback, custom).</span></span>

<span data-ttu-id="d05f7-123">El entorno de tiempo de ejecución principal validará lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d05f7-123">The core runtime will validate the following:</span></span>

-   <span data-ttu-id="d05f7-124">*AlignedBufferOffset* es un múltiplo de 8 bytes</span><span class="sxs-lookup"><span data-stu-id="d05f7-124">*AlignedBufferOffset* is a multiple of 8 bytes</span></span>
-   <span data-ttu-id="d05f7-125">El recurso es un búfer</span><span class="sxs-lookup"><span data-stu-id="d05f7-125">The resource is a buffer</span></span>
-   <span data-ttu-id="d05f7-126">La operación es un miembro válido de la enumeración</span><span class="sxs-lookup"><span data-stu-id="d05f7-126">The operation is a valid member of the enumeration</span></span>
-   <span data-ttu-id="d05f7-127">No se puede llamar a [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) desde una agrupación</span><span class="sxs-lookup"><span data-stu-id="d05f7-127">[**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) cannot be called from within a bundle</span></span>
-   <span data-ttu-id="d05f7-128">El tipo de lista de comandos admite predication</span><span class="sxs-lookup"><span data-stu-id="d05f7-128">The command list type supports predication</span></span>
-   <span data-ttu-id="d05f7-129">El desplazamiento no supera el tamaño del búfer</span><span class="sxs-lookup"><span data-stu-id="d05f7-129">The offset does not exceed the buffer size</span></span>

<span data-ttu-id="d05f7-130">La capa de depuración emitirá un error si el búfer de origen no está en el [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (que es igual que [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)y simplemente un alias).</span><span class="sxs-lookup"><span data-stu-id="d05f7-130">The debug layer will issue an error if the source buffer is not in the [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (which is the same as [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states), and simply an alias) state.</span></span>

<span data-ttu-id="d05f7-131">El conjunto de operaciones que se pueden predicar es:</span><span class="sxs-lookup"><span data-stu-id="d05f7-131">The set of operations which can be predicated are:</span></span>

-   [<span data-ttu-id="d05f7-132">**DrawInstanced**</span><span class="sxs-lookup"><span data-stu-id="d05f7-132">**DrawInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [<span data-ttu-id="d05f7-133">**DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="d05f7-133">**DrawIndexedInstanced**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [<span data-ttu-id="d05f7-134">**Dispatch**</span><span class="sxs-lookup"><span data-stu-id="d05f7-134">**Dispatch**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [<span data-ttu-id="d05f7-135">**CopyTextureRegion**</span><span class="sxs-lookup"><span data-stu-id="d05f7-135">**CopyTextureRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [<span data-ttu-id="d05f7-136">**CopyBufferRegion**</span><span class="sxs-lookup"><span data-stu-id="d05f7-136">**CopyBufferRegion**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [<span data-ttu-id="d05f7-137">**CopyResource**</span><span class="sxs-lookup"><span data-stu-id="d05f7-137">**CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [<span data-ttu-id="d05f7-138">**CopyTiles**</span><span class="sxs-lookup"><span data-stu-id="d05f7-138">**CopyTiles**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [<span data-ttu-id="d05f7-139">**ResolveSubresource**</span><span class="sxs-lookup"><span data-stu-id="d05f7-139">**ResolveSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [<span data-ttu-id="d05f7-140">**ClearDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="d05f7-140">**ClearDepthStencilView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [<span data-ttu-id="d05f7-141">**ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="d05f7-141">**ClearRenderTargetView**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [<span data-ttu-id="d05f7-142">**ClearUnorderedAccessViewUint**</span><span class="sxs-lookup"><span data-stu-id="d05f7-142">**ClearUnorderedAccessViewUint**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [<span data-ttu-id="d05f7-143">**ClearUnorderedAccessViewFloat**</span><span class="sxs-lookup"><span data-stu-id="d05f7-143">**ClearUnorderedAccessViewFloat**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [<span data-ttu-id="d05f7-144">**ExecuteIndirect**</span><span class="sxs-lookup"><span data-stu-id="d05f7-144">**ExecuteIndirect**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

<span data-ttu-id="d05f7-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) no está predicado a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="d05f7-145">[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) is not predicated itself.</span></span> <span data-ttu-id="d05f7-146">En su lugar, se predican las operaciones individuales de la lista anterior que se encuentran en el lado de la agrupación.</span><span class="sxs-lookup"><span data-stu-id="d05f7-146">Instead, individual operations from the list above which are contained in side of the bundle are predicated.</span></span>

<span data-ttu-id="d05f7-147">No se predican los métodos ID3D12GraphicsCommandList [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) y [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) .</span><span class="sxs-lookup"><span data-stu-id="d05f7-147">The ID3D12GraphicsCommandList methods [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) and [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) are not predicated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d05f7-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d05f7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d05f7-149">Contadores y consultas</span><span class="sxs-lookup"><span data-stu-id="d05f7-149">Counters and Queries</span></span>](counters-and-queries.md)
</dt> <dt>

[<span data-ttu-id="d05f7-150">Medición del rendimiento</span><span class="sxs-lookup"><span data-stu-id="d05f7-150">Performance Measurement</span></span>](performance-measurement.md)
</dt> <dt>

[<span data-ttu-id="d05f7-151">Tutoriales de consultas de Predication</span><span class="sxs-lookup"><span data-stu-id="d05f7-151">Predication queries walk-through</span></span>](predication-queries.md)
</dt> </dl>

 

 




