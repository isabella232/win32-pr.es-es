---
title: Nivel de característica 12 Core 1.0 de Direct3D
description: El nivel de característica Core 1,0 es un subconjunto del conjunto completo de características de Direct3D 12.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 42d13b71c516e55ecce378cf9cb415c45e520ba9
ms.sourcegitcommit: bba068130240d16de8a3f3468b7cd72b2cd760f6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/03/2020
ms.locfileid: "105720142"
---
# <a name="the-direct3d-12-core-10-feature-level"></a><span data-ttu-id="c0843-103">Nivel de característica 12 Core 1.0 de Direct3D</span><span class="sxs-lookup"><span data-stu-id="c0843-103">The Direct3D 12 Core 1.0 Feature Level</span></span>

<span data-ttu-id="c0843-104">El nivel de característica Core 1,0 es un subconjunto del conjunto completo de características de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="c0843-104">The Core 1.0 Feature Level is a subset of the full Direct3D 12 feature set.</span></span> <span data-ttu-id="c0843-105">El nivel de característica Core 1,0 se puede exponer mediante una categoría de dispositivos conocidos como *dispositivos solo de proceso*.</span><span class="sxs-lookup"><span data-stu-id="c0843-105">Core 1.0 Feature Level can be exposed by a category of devices known as *compute-only devices*.</span></span> <span data-ttu-id="c0843-106">El modelo general de controladores para los dispositivos solo de proceso es el modelo de controladores de proceso de Microsoft (MCDM).</span><span class="sxs-lookup"><span data-stu-id="c0843-106">The overall driver model for compute-only devices is the Microsoft Compute Driver Model (MCDM).</span></span> <span data-ttu-id="c0843-107">MCDM es un elemento del mismo nivel de reducción horizontal del modelo de controladores de dispositivos de Windows (WDDM), que tiene un ámbito mayor.</span><span class="sxs-lookup"><span data-stu-id="c0843-107">MCDM is a scaled-down peer of the Windows Device Driver Model (WDDM), which has a larger scope.</span></span>

<span data-ttu-id="c0843-108">Un dispositivo que admite *solo* las características dentro de un nivel de característica principal se conoce como *dispositivo principal*.</span><span class="sxs-lookup"><span data-stu-id="c0843-108">A device that supports *only* the features within a Core Feature Level is known as a *Core device*.</span></span>

> [!NOTE]
> <span data-ttu-id="c0843-109">El dispositivo *solo de proceso*, el dispositivo *MCDM*, el dispositivo de *nivel de característica principal* y el *dispositivo principal* significan lo mismo.</span><span class="sxs-lookup"><span data-stu-id="c0843-109">*Compute-only device*, *MCDM device*, *Core Feature Level device*, and *Core device* all mean the same thing.</span></span> <span data-ttu-id="c0843-110">Preferiríamos que el *dispositivo principal* resulte más sencillo.</span><span class="sxs-lookup"><span data-stu-id="c0843-110">We'll prefer *Core device* for simplicity.</span></span>

## <a name="creating-a-core-device"></a><span data-ttu-id="c0843-111">Creación de un dispositivo principal</span><span class="sxs-lookup"><span data-stu-id="c0843-111">Creating a Core device</span></span>

<span data-ttu-id="c0843-112">En general, para crear un dispositivo de Direct3D 12, llame a la función [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) y especifique un nivel de característica mínimo.</span><span class="sxs-lookup"><span data-stu-id="c0843-112">In general, to create a Direct3D 12 device, you call the [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) function, and specify a minimum feature level.</span></span>

<span data-ttu-id="c0843-113">Si especifica un nivel de característica de 9 a 12, el dispositivo que se devuelve es un dispositivo con características enriquecidas, como una GPU tradicional (que admite un supraconjunto de la funcionalidad de un dispositivo principal).</span><span class="sxs-lookup"><span data-stu-id="c0843-113">If you specify a feature level of 9 through 12, then the device that's returned is a feature-rich device, such as a traditional GPU (which supports a superset of the functionality of a Core device).</span></span> <span data-ttu-id="c0843-114">Nunca se devuelve un dispositivo principal para ese intervalo de niveles de características.</span><span class="sxs-lookup"><span data-stu-id="c0843-114">A Core device is never returned for that range of feature levels.</span></span>

<span data-ttu-id="c0843-115">Por otro lado, si especifica un nivel de característica principal (por ejemplo, [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), el dispositivo devuelto podría ser rico en características, o podría ser un dispositivo principal.</span><span class="sxs-lookup"><span data-stu-id="c0843-115">On the other hand, if you specify a Core feature level (for example, [**D3D_FEATURE_LEVEL::D3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), then the device that's returned could be feature-rich, or it could be a Core device.</span></span>

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

<span data-ttu-id="c0843-116">Si especifica un `_CORE` nivel de característica, el nivel de tiempo de ejecución o de depuración valida que las características que usa la aplicación se permiten en ese `_CORE` nivel de características.</span><span class="sxs-lookup"><span data-stu-id="c0843-116">If you specify a `_CORE` feature level, then the runtime/debug layer validates that the features your application uses are allowed by that `_CORE` feature level.</span></span> <span data-ttu-id="c0843-117">Este conjunto de características se define más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="c0843-117">That set of features is defined later in this topic.</span></span>

## <a name="shader-model-for-core-devices"></a><span data-ttu-id="c0843-118">Modelo de sombreador para dispositivos principales</span><span class="sxs-lookup"><span data-stu-id="c0843-118">Shader model for Core devices</span></span>

<span data-ttu-id="c0843-119">Un dispositivo principal es compatible con el modelo de sombreador 5.0 +.</span><span class="sxs-lookup"><span data-stu-id="c0843-119">A Core device supports Shader Model 5.0+.</span></span>

<span data-ttu-id="c0843-120">El motor en tiempo de ejecución realiza la conversión de los modelos de sombreador no DXIL de 5. x a 6,0 DXIL.</span><span class="sxs-lookup"><span data-stu-id="c0843-120">The runtime performs conversion of 5.x non DXIL shader models to 6.0 DXIL.</span></span> <span data-ttu-id="c0843-121">Por lo tanto, el controlador solo necesita admitir 6. x.</span><span class="sxs-lookup"><span data-stu-id="c0843-121">So the driver need only support 6.x.</span></span>

## <a name="resource-management-model-for-core-devices"></a><span data-ttu-id="c0843-122">Modelo de administración de recursos para dispositivos principales</span><span class="sxs-lookup"><span data-stu-id="c0843-122">Resource management model for Core devices</span></span>

- <span data-ttu-id="c0843-123">Dimensiones de recursos compatibles: solo búferes sin formato y estructurados (sin búferes con tipo, texture1d/2D, etc.)</span><span class="sxs-lookup"><span data-stu-id="c0843-123">Supported resource dimensions: raw and structured buffers only (no typed buffers, texture1d/2D, etc.)</span></span>
- <span data-ttu-id="c0843-124">No se admiten recursos reservados (en mosaico)</span><span class="sxs-lookup"><span data-stu-id="c0843-124">No support for reserved (tiled) resources</span></span>
- <span data-ttu-id="c0843-125">No se admiten montones personalizados</span><span class="sxs-lookup"><span data-stu-id="c0843-125">No support for custom heaps</span></span>
- <span data-ttu-id="c0843-126">No se admite ninguna de estas marcas de montón:</span><span class="sxs-lookup"><span data-stu-id="c0843-126">No support for any of these heap flags:</span></span>
  - <span data-ttu-id="c0843-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span><span class="sxs-lookup"><span data-stu-id="c0843-127">D3D12_HEAP_FLAG_HARDWARE_PROTECTED</span></span>
  - <span data-ttu-id="c0843-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span><span class="sxs-lookup"><span data-stu-id="c0843-128">D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH</span></span>
  - <span data-ttu-id="c0843-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span><span class="sxs-lookup"><span data-stu-id="c0843-129">D3D12_HEAP_FLAG_ALLOW_DISPLAY</span></span>
  - <span data-ttu-id="c0843-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (tenga en cuenta que el sombreador de nota atómicas es necesario, esta marca es para otra característica, atomices de adaptador cruzado)</span><span class="sxs-lookup"><span data-stu-id="c0843-130">D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (note shader atomics are required, this flag is for another feature, cross adapter atomics)</span></span>

## <a name="resource-binding-model-for-core-devices"></a><span data-ttu-id="c0843-131">Modelo de enlace de recursos para dispositivos principales</span><span class="sxs-lookup"><span data-stu-id="c0843-131">Resource binding model for Core devices</span></span>

- <span data-ttu-id="c0843-132">Compatibilidad solo con el nivel 1 del enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="c0843-132">Support for resource binding tier 1 only</span></span>
- <span data-ttu-id="c0843-133">Excepciones:</span><span class="sxs-lookup"><span data-stu-id="c0843-133">Exceptions:</span></span>
  - <span data-ttu-id="c0843-134">No se admiten los muestreadores de textura</span><span class="sxs-lookup"><span data-stu-id="c0843-134">No support for texture samplers</span></span>
  - <span data-ttu-id="c0843-135">Compatibilidad con 64 UAVs como el nivel de característica 11.1 + (en lugar de 8)</span><span class="sxs-lookup"><span data-stu-id="c0843-135">Support for 64 UAVs like Feature Level 11.1+ (as opposed to only 8)</span></span>
  - <span data-ttu-id="c0843-136">Las implementaciones no tienen que implementar la comprobación de los límites en los accesos de sombreador a los recursos a través de descriptores, y los accesos fuera de los límites producen un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="c0843-136">Implementations do not have to implement bounds checking on shader accesses to resources through descriptors, out of bounds accesses produce undefined behavior.</span></span>
    - <span data-ttu-id="c0843-137">Como subproducto, no se admite la marca de intervalo de descriptor D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS en las signaturas raíz.</span><span class="sxs-lookup"><span data-stu-id="c0843-137">As a byproduct, the descriptor range flag D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS in root signatures is not supported.</span></span>
- <span data-ttu-id="c0843-138">Los descriptores de UAV/CBV solo se pueden realizar en recursos de montones predeterminados (por lo que no hay montones de carga/readback).</span><span class="sxs-lookup"><span data-stu-id="c0843-138">UAV/CBV descriptors can only be made on resources from default heaps (so no upload/readback heaps).</span></span> <span data-ttu-id="c0843-139">Esto obliga a la aplicación a realizar copias para obtener datos entre la CPU< >GPU.</span><span class="sxs-lookup"><span data-stu-id="c0843-139">This forces your application to do copies to get data across CPU<->GPU.</span></span>
- <span data-ttu-id="c0843-140">A pesar de ser el nivel de capacidad de enlace más bajo, todavía hay algunas características necesarias, incluso en este nivel, que vale la pena llamar:</span><span class="sxs-lookup"><span data-stu-id="c0843-140">Despite being the lowest binding capability tier, there are still some features required even in this tier worth calling out:</span></span>
  - <span data-ttu-id="c0843-141">Los montones de descriptores se pueden actualizar una vez que se registran las listas de comandos (vea D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE en la especificación de enlace de recursos)</span><span class="sxs-lookup"><span data-stu-id="c0843-141">Descriptor heaps can be updated after command lists are recorded (see D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE in the resource binding spec)</span></span>
  - <span data-ttu-id="c0843-142">Los descriptores raíz son básicamente punteros GPUVA</span><span class="sxs-lookup"><span data-stu-id="c0843-142">Root descriptors are basically GPUVA pointers</span></span>
    - <span data-ttu-id="c0843-143">Aunque no se admiten MMU/VA, el búfer VAs que se usa en los descriptores raíz se puede emular mediante implementaciones mediante la aplicación de revisiones de direcciones.</span><span class="sxs-lookup"><span data-stu-id="c0843-143">Even though there is no MMU / VA support, buffer VAs that are used in root descriptors can be emulated by implementations by doing address patching.</span></span>

### <a name="structured-buffer-restrictions"></a><span data-ttu-id="c0843-144">Restricciones de búfer estructurado</span><span class="sxs-lookup"><span data-stu-id="c0843-144">Structured buffer restrictions</span></span>

<span data-ttu-id="c0843-145">Los búferes estructurados deben tener una dirección base con una alineación de 4 bytes y el intervalo debe ser 2 o un múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="c0843-145">Structured buffers must have a base address that is 4 byte aligned, and stride must be 2 or a multiple of 4.</span></span> <span data-ttu-id="c0843-146">El caso de un paso de 2 es para aplicaciones con datos de 16 bits, especialmente dado que no se admiten búferes con tipo en D3D_FEATURE_LEVEL_1_0_CORE.</span><span class="sxs-lookup"><span data-stu-id="c0843-146">The case for a stride of 2 is for apps with 16 bit data, particularly given there is no support for typed buffers in D3D_FEATURE_LEVEL_1_0_CORE.</span></span>

<span data-ttu-id="c0843-147">El intervalo especificado en los descriptores debe coincidir con el intervalo especificado en HLSL.</span><span class="sxs-lookup"><span data-stu-id="c0843-147">Stride specified in descriptors must match the stride specified in HLSL.</span></span>  

## <a name="command-queue-support-for-core-devices"></a><span data-ttu-id="c0843-148">Compatibilidad de cola de comandos para dispositivos principales</span><span class="sxs-lookup"><span data-stu-id="c0843-148">Command queue support for Core devices</span></span>

<span data-ttu-id="c0843-149">Compute y Copy Queues Only (no 3D, vídeo, etc.).</span><span class="sxs-lookup"><span data-stu-id="c0843-149">Compute and copy queues only (no 3D, video, etc. queues).</span></span>

## <a name="shader-support-for-core-devices"></a><span data-ttu-id="c0843-150">Compatibilidad del sombreador con dispositivos principales</span><span class="sxs-lookup"><span data-stu-id="c0843-150">Shader support for Core devices</span></span>

<span data-ttu-id="c0843-151">Solo para los sombreadores de cálculo, sin sombreadores de gráficos (vértices, sombreadores de píxeles, etc.) ni ninguna funcionalidad relacionada, como destinos de representación, cadenas de intercambio, ensamblador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0843-151">Compute shaders only, no graphics shaders (Vertex, Pixel Shaders, etc.) nor any related functionality such as render targets, swap chains, input assembler.</span></span>

### <a name="arithmetic-precision"></a><span data-ttu-id="c0843-152">Precisión aritmética</span><span class="sxs-lookup"><span data-stu-id="c0843-152">Arithmetic precision</span></span>

<span data-ttu-id="c0843-153">Los dispositivos principales no tienen que admitir desnormativas para operaciones de punto flotante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c0843-153">Core devices do not have to support denorms for 16 bit floating point operations.</span></span>

## <a name="supported-apis-for-core-devices"></a><span data-ttu-id="c0843-154">API admitidas para dispositivos principales</span><span class="sxs-lookup"><span data-stu-id="c0843-154">Supported APIs for Core devices</span></span>

<span data-ttu-id="c0843-155">La siguiente lista representa el subconjunto admitido de la interfaz de programación de aplicaciones completa (las API que *no* se admiten en el nivel de características Core 1,0 *no* aparecen en la lista).</span><span class="sxs-lookup"><span data-stu-id="c0843-155">The list below represents the supported subset of the full application programming interface (APIs that are *not* supported in Core 1.0 Feature Level are *not* listed).</span></span>

### <a name="id3d12device-methods"></a><span data-ttu-id="c0843-156">Métodos ID3D12Device</span><span class="sxs-lookup"><span data-stu-id="c0843-156">ID3D12Device methods</span></span>

* [<span data-ttu-id="c0843-157">ID3D12Device::CheckFeatureSupport</span><span class="sxs-lookup"><span data-stu-id="c0843-157">ID3D12Device::CheckFeatureSupport</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [<span data-ttu-id="c0843-158">ID3D12Device::CopyDescriptors</span><span class="sxs-lookup"><span data-stu-id="c0843-158">ID3D12Device::CopyDescriptors</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [<span data-ttu-id="c0843-159">ID3D12Device::CopyDescriptorsSimple</span><span class="sxs-lookup"><span data-stu-id="c0843-159">ID3D12Device::CopyDescriptorsSimple</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [<span data-ttu-id="c0843-160">ID3D12Device::CreateCommandAllocator</span><span class="sxs-lookup"><span data-stu-id="c0843-160">ID3D12Device::CreateCommandAllocator</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [<span data-ttu-id="c0843-161">ID3D12Device::CreateCommandList</span><span class="sxs-lookup"><span data-stu-id="c0843-161">ID3D12Device::CreateCommandList</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [<span data-ttu-id="c0843-162">ID3D12Device::CreateCommandQueue</span><span class="sxs-lookup"><span data-stu-id="c0843-162">ID3D12Device::CreateCommandQueue</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [<span data-ttu-id="c0843-163">ID3D12Device::CreateCommandSignature</span><span class="sxs-lookup"><span data-stu-id="c0843-163">ID3D12Device::CreateCommandSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [<span data-ttu-id="c0843-164">ID3D12Device::CreateCommittedResource</span><span class="sxs-lookup"><span data-stu-id="c0843-164">ID3D12Device::CreateCommittedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [<span data-ttu-id="c0843-165">ID3D12Device::CreateComputePipelineState</span><span class="sxs-lookup"><span data-stu-id="c0843-165">ID3D12Device::CreateComputePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [<span data-ttu-id="c0843-166">ID3D12Device::CreateConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="c0843-166">ID3D12Device::CreateConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [<span data-ttu-id="c0843-167">ID3D12Device::CreateDescriptorHeap</span><span class="sxs-lookup"><span data-stu-id="c0843-167">ID3D12Device::CreateDescriptorHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [<span data-ttu-id="c0843-168">ID3D12Device::CreateFence</span><span class="sxs-lookup"><span data-stu-id="c0843-168">ID3D12Device::CreateFence</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [<span data-ttu-id="c0843-169">ID3D12Device::CreateHeap</span><span class="sxs-lookup"><span data-stu-id="c0843-169">ID3D12Device::CreateHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [<span data-ttu-id="c0843-170">ID3D12Device::CreatePlacedResource</span><span class="sxs-lookup"><span data-stu-id="c0843-170">ID3D12Device::CreatePlacedResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [<span data-ttu-id="c0843-171">ID3D12Device::CreateQueryHeap</span><span class="sxs-lookup"><span data-stu-id="c0843-171">ID3D12Device::CreateQueryHeap</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [<span data-ttu-id="c0843-172">ID3D12Device::CreateRootSignature</span><span class="sxs-lookup"><span data-stu-id="c0843-172">ID3D12Device::CreateRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [<span data-ttu-id="c0843-173">ID3D12Device::CreateShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="c0843-173">ID3D12Device::CreateShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [<span data-ttu-id="c0843-174">ID3D12Device::CreateSharedHandle</span><span class="sxs-lookup"><span data-stu-id="c0843-174">ID3D12Device::CreateSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [<span data-ttu-id="c0843-175">ID3D12Device::CreateUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="c0843-175">ID3D12Device::CreateUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [<span data-ttu-id="c0843-176">ID3D12Device:: expulsión</span><span class="sxs-lookup"><span data-stu-id="c0843-176">ID3D12Device::Evict</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [<span data-ttu-id="c0843-177">ID3D12Device::GetAdapterLuid</span><span class="sxs-lookup"><span data-stu-id="c0843-177">ID3D12Device::GetAdapterLuid</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [<span data-ttu-id="c0843-178">ID3D12Device::GetCopyableFootprints</span><span class="sxs-lookup"><span data-stu-id="c0843-178">ID3D12Device::GetCopyableFootprints</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [<span data-ttu-id="c0843-179">ID3D12Device::GetCustomHeapProperties</span><span class="sxs-lookup"><span data-stu-id="c0843-179">ID3D12Device::GetCustomHeapProperties</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [<span data-ttu-id="c0843-180">ID3D12Device::GetDescriptorHandleIncrementSize</span><span class="sxs-lookup"><span data-stu-id="c0843-180">ID3D12Device::GetDescriptorHandleIncrementSize</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [<span data-ttu-id="c0843-181">ID3D12Device::GetDeviceRemovedReason</span><span class="sxs-lookup"><span data-stu-id="c0843-181">ID3D12Device::GetDeviceRemovedReason</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [<span data-ttu-id="c0843-182">ID3D12Device::GetNodeCount</span><span class="sxs-lookup"><span data-stu-id="c0843-182">ID3D12Device::GetNodeCount</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [<span data-ttu-id="c0843-183">ID3D12Device::GetResourceAllocationInfo</span><span class="sxs-lookup"><span data-stu-id="c0843-183">ID3D12Device::GetResourceAllocationInfo</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [<span data-ttu-id="c0843-184">ID3D12Device::MakeResident</span><span class="sxs-lookup"><span data-stu-id="c0843-184">ID3D12Device::MakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [<span data-ttu-id="c0843-185">ID3D12Device::OpenSharedHandle</span><span class="sxs-lookup"><span data-stu-id="c0843-185">ID3D12Device::OpenSharedHandle</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [<span data-ttu-id="c0843-186">ID3D12Device::OpenSharedHandleByName</span><span class="sxs-lookup"><span data-stu-id="c0843-186">ID3D12Device::OpenSharedHandleByName</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [<span data-ttu-id="c0843-187">ID3D12Device::SetStablePowerState</span><span class="sxs-lookup"><span data-stu-id="c0843-187">ID3D12Device::SetStablePowerState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a><span data-ttu-id="c0843-188">Métodos ID3D12Device1</span><span class="sxs-lookup"><span data-stu-id="c0843-188">ID3D12Device1 methods</span></span>

* [<span data-ttu-id="c0843-189">ID3D12Device1::CreatePipelineLibrary</span><span class="sxs-lookup"><span data-stu-id="c0843-189">ID3D12Device1::CreatePipelineLibrary</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [<span data-ttu-id="c0843-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span><span class="sxs-lookup"><span data-stu-id="c0843-190">ID3D12Device1::SetEventOnMultipleFenceCompletion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [<span data-ttu-id="c0843-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span><span class="sxs-lookup"><span data-stu-id="c0843-191">ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a><span data-ttu-id="c0843-192">Métodos ID3D12Device2</span><span class="sxs-lookup"><span data-stu-id="c0843-192">ID3D12Device2 methods</span></span>

* [<span data-ttu-id="c0843-193">ID3D12Device2::CreatePipelineState</span><span class="sxs-lookup"><span data-stu-id="c0843-193">ID3D12Device2::CreatePipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a><span data-ttu-id="c0843-194">Métodos ID3D12Device3</span><span class="sxs-lookup"><span data-stu-id="c0843-194">ID3D12Device3 methods</span></span>

* [<span data-ttu-id="c0843-195">ID3D12Device3::OpenExistingHeapFromAddress</span><span class="sxs-lookup"><span data-stu-id="c0843-195">ID3D12Device3::OpenExistingHeapFromAddress</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* <span data-ttu-id="c0843-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span><span class="sxs-lookup"><span data-stu-id="c0843-196">[ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))</span></span>
* [<span data-ttu-id="c0843-197">ID3D12Device3::EnqueueMakeResident</span><span class="sxs-lookup"><span data-stu-id="c0843-197">ID3D12Device3::EnqueueMakeResident</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a><span data-ttu-id="c0843-198">Métodos ID3D12Device4</span><span class="sxs-lookup"><span data-stu-id="c0843-198">ID3D12Device4 methods</span></span>

* [<span data-ttu-id="c0843-199">ID3D12Device4::GetResourceAllocationInfo1</span><span class="sxs-lookup"><span data-stu-id="c0843-199">ID3D12Device4::GetResourceAllocationInfo1</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a><span data-ttu-id="c0843-200">Métodos ID3D12Device5</span><span class="sxs-lookup"><span data-stu-id="c0843-200">ID3D12Device5 methods</span></span>

* [<span data-ttu-id="c0843-201">ID3D12Device5::CreateMetaCommand</span><span class="sxs-lookup"><span data-stu-id="c0843-201">ID3D12Device5::CreateMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [<span data-ttu-id="c0843-202">ID3D12Device5::CreateStateObject</span><span class="sxs-lookup"><span data-stu-id="c0843-202">ID3D12Device5::CreateStateObject</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [<span data-ttu-id="c0843-203">ID3D12Device5::EnumerateMetaCommandParameters</span><span class="sxs-lookup"><span data-stu-id="c0843-203">ID3D12Device5::EnumerateMetaCommandParameters</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [<span data-ttu-id="c0843-204">ID3D12Device5::EnumerateMetaCommands</span><span class="sxs-lookup"><span data-stu-id="c0843-204">ID3D12Device5::EnumerateMetaCommands</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [<span data-ttu-id="c0843-205">ID3D12Device5::RemoveDevice</span><span class="sxs-lookup"><span data-stu-id="c0843-205">ID3D12Device5::RemoveDevice</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a><span data-ttu-id="c0843-206">Métodos ID3D12CommandQueue</span><span class="sxs-lookup"><span data-stu-id="c0843-206">ID3D12CommandQueue methods</span></span>

* [<span data-ttu-id="c0843-207">ID3D12CommandQueue::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="c0843-207">ID3D12CommandQueue::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [<span data-ttu-id="c0843-208">ID3D12CommandQueue::EndEvent</span><span class="sxs-lookup"><span data-stu-id="c0843-208">ID3D12CommandQueue::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [<span data-ttu-id="c0843-209">ID3D12CommandQueue::ExecuteCommandLists</span><span class="sxs-lookup"><span data-stu-id="c0843-209">ID3D12CommandQueue::ExecuteCommandLists</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [<span data-ttu-id="c0843-210">ID3D12CommandQueue::GetClockCalibration</span><span class="sxs-lookup"><span data-stu-id="c0843-210">ID3D12CommandQueue::GetClockCalibration</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [<span data-ttu-id="c0843-211">ID3D12CommandQueue::GetDesc</span><span class="sxs-lookup"><span data-stu-id="c0843-211">ID3D12CommandQueue::GetDesc</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [<span data-ttu-id="c0843-212">ID3D12CommandQueue::GetTimestampFrequency</span><span class="sxs-lookup"><span data-stu-id="c0843-212">ID3D12CommandQueue::GetTimestampFrequency</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [<span data-ttu-id="c0843-213">ID3D12CommandQueue::SetMarker</span><span class="sxs-lookup"><span data-stu-id="c0843-213">ID3D12CommandQueue::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [<span data-ttu-id="c0843-214">ID3D12CommandQueue:: Signal</span><span class="sxs-lookup"><span data-stu-id="c0843-214">ID3D12CommandQueue::Signal</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [<span data-ttu-id="c0843-215">ID3D12CommandQueue:: wait</span><span class="sxs-lookup"><span data-stu-id="c0843-215">ID3D12CommandQueue::Wait</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a><span data-ttu-id="c0843-216">Métodos ID3D12CommandList</span><span class="sxs-lookup"><span data-stu-id="c0843-216">ID3D12CommandList methods</span></span>

* [<span data-ttu-id="c0843-217">ID3D12CommandList:: GetType</span><span class="sxs-lookup"><span data-stu-id="c0843-217">ID3D12CommandList::GetType</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a><span data-ttu-id="c0843-218">Métodos ID3D12GraphicsCommandList</span><span class="sxs-lookup"><span data-stu-id="c0843-218">ID3D12GraphicsCommandList methods</span></span>

* [<span data-ttu-id="c0843-219">ID3D12GraphicsCommandList::BeginEvent</span><span class="sxs-lookup"><span data-stu-id="c0843-219">ID3D12GraphicsCommandList::BeginEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [<span data-ttu-id="c0843-220">ID3D12GraphicsCommandList::BeginQuery</span><span class="sxs-lookup"><span data-stu-id="c0843-220">ID3D12GraphicsCommandList::BeginQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [<span data-ttu-id="c0843-221">ID3D12GraphicsCommandList::ClearState</span><span class="sxs-lookup"><span data-stu-id="c0843-221">ID3D12GraphicsCommandList::ClearState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [<span data-ttu-id="c0843-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span><span class="sxs-lookup"><span data-stu-id="c0843-222">ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [<span data-ttu-id="c0843-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span><span class="sxs-lookup"><span data-stu-id="c0843-223">ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [<span data-ttu-id="c0843-224">ID3D12GraphicsCommandList:: Close</span><span class="sxs-lookup"><span data-stu-id="c0843-224">ID3D12GraphicsCommandList::Close</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [<span data-ttu-id="c0843-225">ID3D12GraphicsCommandList::CopyBufferRegion</span><span class="sxs-lookup"><span data-stu-id="c0843-225">ID3D12GraphicsCommandList::CopyBufferRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [<span data-ttu-id="c0843-226">ID3D12GraphicsCommandList::CopyResource</span><span class="sxs-lookup"><span data-stu-id="c0843-226">ID3D12GraphicsCommandList::CopyResource</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [<span data-ttu-id="c0843-227">ID3D12GraphicsCommandList::CopyTextureRegion</span><span class="sxs-lookup"><span data-stu-id="c0843-227">ID3D12GraphicsCommandList::CopyTextureRegion</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [<span data-ttu-id="c0843-228">ID3D12GraphicsCommandList::D ispatch</span><span class="sxs-lookup"><span data-stu-id="c0843-228">ID3D12GraphicsCommandList::Dispatch</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [<span data-ttu-id="c0843-229">ID3D12GraphicsCommandList::EndEvent</span><span class="sxs-lookup"><span data-stu-id="c0843-229">ID3D12GraphicsCommandList::EndEvent</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [<span data-ttu-id="c0843-230">ID3D12GraphicsCommandList::EndQuery</span><span class="sxs-lookup"><span data-stu-id="c0843-230">ID3D12GraphicsCommandList::EndQuery</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [<span data-ttu-id="c0843-231">ID3D12GraphicsCommandList:: RESET</span><span class="sxs-lookup"><span data-stu-id="c0843-231">ID3D12GraphicsCommandList::Reset</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [<span data-ttu-id="c0843-232">ID3D12GraphicsCommandList::ResolveQueryData</span><span class="sxs-lookup"><span data-stu-id="c0843-232">ID3D12GraphicsCommandList::ResolveQueryData</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [<span data-ttu-id="c0843-233">ID3D12GraphicsCommandList::ResourceBarrier</span><span class="sxs-lookup"><span data-stu-id="c0843-233">ID3D12GraphicsCommandList::ResourceBarrier</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [<span data-ttu-id="c0843-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span><span class="sxs-lookup"><span data-stu-id="c0843-234">ID3D12GraphicsCommandList::SetComputeRoot32BitConstant</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [<span data-ttu-id="c0843-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span><span class="sxs-lookup"><span data-stu-id="c0843-235">ID3D12GraphicsCommandList::SetComputeRoot32BitConstants</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [<span data-ttu-id="c0843-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span><span class="sxs-lookup"><span data-stu-id="c0843-236">ID3D12GraphicsCommandList::SetComputeRootConstantBufferView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [<span data-ttu-id="c0843-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="c0843-237">ID3D12GraphicsCommandList::SetComputeRootDescriptorTable</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [<span data-ttu-id="c0843-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span><span class="sxs-lookup"><span data-stu-id="c0843-238">ID3D12GraphicsCommandList::SetComputeRootShaderResourceView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [<span data-ttu-id="c0843-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span><span class="sxs-lookup"><span data-stu-id="c0843-239">ID3D12GraphicsCommandList::SetComputeRootSignature</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [<span data-ttu-id="c0843-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="c0843-240">ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [<span data-ttu-id="c0843-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span><span class="sxs-lookup"><span data-stu-id="c0843-241">ID3D12GraphicsCommandList::SetDescriptorHeaps</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [<span data-ttu-id="c0843-242">ID3D12GraphicsCommandList::SetMarker</span><span class="sxs-lookup"><span data-stu-id="c0843-242">ID3D12GraphicsCommandList::SetMarker</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [<span data-ttu-id="c0843-243">ID3D12GraphicsCommandList::SetPipelineState</span><span class="sxs-lookup"><span data-stu-id="c0843-243">ID3D12GraphicsCommandList::SetPipelineState</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [<span data-ttu-id="c0843-244">ID3D12GraphicsCommandList::SetPredication</span><span class="sxs-lookup"><span data-stu-id="c0843-244">ID3D12GraphicsCommandList::SetPredication</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a><span data-ttu-id="c0843-245">Métodos ID3D12GraphicsCommandList1</span><span class="sxs-lookup"><span data-stu-id="c0843-245">ID3D12GraphicsCommandList1 methods</span></span>

* [<span data-ttu-id="c0843-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span><span class="sxs-lookup"><span data-stu-id="c0843-246">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [<span data-ttu-id="c0843-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span><span class="sxs-lookup"><span data-stu-id="c0843-247">ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a><span data-ttu-id="c0843-248">Métodos ID3D12GraphicsCommandList2</span><span class="sxs-lookup"><span data-stu-id="c0843-248">ID3D12GraphicsCommandList2 methods</span></span>

* [<span data-ttu-id="c0843-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span><span class="sxs-lookup"><span data-stu-id="c0843-249">ID3D12GraphicsCommandList2::WriteBufferImmediate</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a><span data-ttu-id="c0843-250">Métodos ID3D12GraphicsCommandList4</span><span class="sxs-lookup"><span data-stu-id="c0843-250">ID3D12GraphicsCommandList4 methods</span></span>

* [<span data-ttu-id="c0843-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span><span class="sxs-lookup"><span data-stu-id="c0843-251">ID3D12GraphicsCommandList4::ExecuteMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [<span data-ttu-id="c0843-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span><span class="sxs-lookup"><span data-stu-id="c0843-252">ID3D12GraphicsCommandList4::InitializeMetaCommand</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
