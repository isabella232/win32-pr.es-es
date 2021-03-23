---
title: Validación basada en GPU y nivel de depuración de Direct3D 12
description: En este tema se describe cómo hacer el mejor uso de la capa de depuración de Direct3D 12. La validación basada en GPU (GBV) permite escenarios de validación en la escala de tiempo de GPU que no son posibles durante las llamadas API en la CPU.
ms.assetid: 01D1F94F-4DD4-4781-86EF-6C639E8B1069
ms.localizationpriority: high
ms.topic: article
ms.date: 02/12/2019
ms.openlocfilehash: 3160df3faf994df2abf9cf878088e84564bb5fe1
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104549163"
---
# <a name="gpu-based-validation-and-the-direct3d-12-debug-layer"></a><span data-ttu-id="9de93-104">Validación basada en GPU y nivel de depuración de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9de93-104">GPU-based validation and the Direct3D 12 Debug Layer</span></span>

<span data-ttu-id="9de93-105">En este tema se describe cómo hacer el mejor uso de la capa de depuración de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9de93-105">This topic describes how to make best use of the Direct3D 12 Debug Layer.</span></span> <span data-ttu-id="9de93-106">La validación basada en GPU (GBV) permite escenarios de validación en la escala de tiempo de GPU que no son posibles durante las llamadas API en la CPU.</span><span class="sxs-lookup"><span data-stu-id="9de93-106">GPU-based validation (GBV) enables validation scenarios on the GPU timeline that are not possible during API calls on the CPU.</span></span> <span data-ttu-id="9de93-107">GBV está disponible a partir de la actualización de aniversario de herramientas de gráficos para Windows 10.</span><span class="sxs-lookup"><span data-stu-id="9de93-107">GBV is available starting with the Graphics Tools for Windows 10 Anniversary Update.</span></span>

## <a name="purpose-of-gpu-based-validation"></a><span data-ttu-id="9de93-108">Finalidad de la validación basada en GPU</span><span class="sxs-lookup"><span data-stu-id="9de93-108">Purpose of GPU-based validation</span></span>

<span data-ttu-id="9de93-109">La validación basada en GPU ayuda a identificar los errores siguientes:</span><span class="sxs-lookup"><span data-stu-id="9de93-109">GPU-based validation helps to identify the following errors:</span></span>

- <span data-ttu-id="9de93-110">Uso de descriptores no inicializados o incompatibles en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="9de93-110">Use of uninitialized or incompatible descriptors in a shader.</span></span>
- <span data-ttu-id="9de93-111">Uso de descriptores que hacen referencia a recursos eliminados en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="9de93-111">Use of descriptors referencing deleted Resources in a shader.</span></span>
- <span data-ttu-id="9de93-112">Validación de los Estados de los recursos promocionados y la caída del estado de los recursos.</span><span class="sxs-lookup"><span data-stu-id="9de93-112">Validation of promoted resource states and resource state decay.</span></span>
- <span data-ttu-id="9de93-113">Indexación más allá del final del montón de descriptores en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="9de93-113">Indexing beyond the end of the descriptor heap in a shader.</span></span>
- <span data-ttu-id="9de93-114">El sombreador tiene acceso a los recursos en estado incompatible.</span><span class="sxs-lookup"><span data-stu-id="9de93-114">Shader accesses of resources in incompatible state.</span></span>
- <span data-ttu-id="9de93-115">Uso de muestras no inicializadas o incompatibles en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="9de93-115">Use of uninitialized or incompatible Samplers in a shader.</span></span>

<span data-ttu-id="9de93-116">GBV funciona mediante la creación de sombreadores revisados que tienen la validación agregada directamente al sombreador.</span><span class="sxs-lookup"><span data-stu-id="9de93-116">GBV works by creating patched shaders that have validation added directly to the shader.</span></span> <span data-ttu-id="9de93-117">Los sombreadores con revisión inspeccionan los argumentos raíz y los recursos a los que se tiene acceso durante la ejecución del sombreador y notifican los errores a un búfer de registro.</span><span class="sxs-lookup"><span data-stu-id="9de93-117">The patched shaders inspect root arguments and resources accessed during shader execution and report errors to a log buffer.</span></span> <span data-ttu-id="9de93-118">GBV también inyecta operaciones adicionales y envía llamadas a las listas de comandos de la aplicación para validar y realizar un seguimiento de los cambios en el estado de los recursos impuesto por la lista de comandos de la escala de tiempo de GPU.</span><span class="sxs-lookup"><span data-stu-id="9de93-118">GBV also injects extra operations and Dispatch calls into the application command lists to validate and track changes to resource state imposed by the command list on the GPU-timeline.</span></span>

<span data-ttu-id="9de93-119">Dado que GBV requiere la capacidad de ejecutar sombreadores, las listas de comandos de copia se emulan mediante una lista de comandos de proceso.</span><span class="sxs-lookup"><span data-stu-id="9de93-119">Because GBV requires the ability to execute shaders, COPY command lists are emulated by a COMPUTE command list.</span></span> <span data-ttu-id="9de93-120">Esto podría cambiar el modo en que el hardware realiza copias, pero el resultado final no debe cambiarse.</span><span class="sxs-lookup"><span data-stu-id="9de93-120">This may potentially change how hardware performs copies though the end result should not be changed.</span></span> <span data-ttu-id="9de93-121">La aplicación seguirá percibiendo que se trata de listas de comandos de copia y el nivel de depuración las validará como tal.</span><span class="sxs-lookup"><span data-stu-id="9de93-121">The application will still perceive these are COPY command lists and the debug layer will validate them as such.</span></span>

## <a name="turning-on-gpu-based-validation"></a><span data-ttu-id="9de93-122">Activar la validación basada en GPU</span><span class="sxs-lookup"><span data-stu-id="9de93-122">Turning on GPU-based validation</span></span>

<span data-ttu-id="9de93-123">Se puede forzar el uso de GBV mediante el panel de control de DirectX (DXCPL) al forzar el nivel de depuración de Direct3D 12 y, además, forzar la validación basada en GPU (nueva pestaña en el panel de control).</span><span class="sxs-lookup"><span data-stu-id="9de93-123">GBV can be forced on using the DirectX Control Panel (DXCPL) by forcing on the Direct3D 12 Debug Layer and additionally forcing on GPU-based validation (new tab in the control panel).</span></span> <span data-ttu-id="9de93-124">Una vez que se haya habilitado, GBV permanecerá habilitado hasta que se libere el dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9de93-124">Once enabled, GBV will remain enabled until the Direct3D 12 device is released.</span></span> <span data-ttu-id="9de93-125">Como alternativa, GBV se puede habilitar mediante programación antes de crear el dispositivo Direct3D 12:</span><span class="sxs-lookup"><span data-stu-id="9de93-125">Alternatively, GBV can be enabled programmatically prior to creating the Direct3D 12 Device:</span></span>

```cpp
void EnableShaderBasedValidation()
{
    CComPtr<ID3D12Debug> spDebugController0;
    CComPtr<ID3D12Debug1> spDebugController1;
    VERIFY(D3D12GetDebugInterface(IID_PPV_ARGS(&spDebugController0)));
    VERIFY(spDebugController0->QueryInterface(IID_PPV_ARGS(&spDebugController1)));
    spDebugController1->SetEnableGPUBasedValidation(true);
}
```

## <a name="recommended-usage"></a><span data-ttu-id="9de93-126">Uso recomendado</span><span class="sxs-lookup"><span data-stu-id="9de93-126">Recommended usage</span></span>

<span data-ttu-id="9de93-127">En general, debe ejecutar el código con la capa de depuración habilitada la mayor parte del tiempo.</span><span class="sxs-lookup"><span data-stu-id="9de93-127">Generally, you should run your code with the debug layer enabled most of the time.</span></span> <span data-ttu-id="9de93-128">Sin embargo, GBV puede ralentizar las cosas.</span><span class="sxs-lookup"><span data-stu-id="9de93-128">However, GBV can slow things down a lot.</span></span> <span data-ttu-id="9de93-129">Los desarrolladores pueden considerar la posibilidad de habilitar GBV con conjuntos de datos más pequeños (por ejemplo, demostraciones del motor o niveles de juegos pequeños con menos recursos y recursos del PSO) o durante el inicio de la aplicación temprana para reducir los problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9de93-129">Developers may consider enabling GBV with smaller data sets (for example, engine demos or small game levels with fewer PSO’s and resources) or during early application bring-up to reduce performance problems.</span></span> <span data-ttu-id="9de93-130">Con contenido más grande, considere la posibilidad de activar GBV en uno o dos equipos de pruebas en un paso de prueba nocturno.</span><span class="sxs-lookup"><span data-stu-id="9de93-130">With larger content consider turning on GBV on one or two test machines in a nightly test pass.</span></span>

## <a name="debug-output"></a><span data-ttu-id="9de93-131">Salida de depuración</span><span class="sxs-lookup"><span data-stu-id="9de93-131">Debug output</span></span>

<span data-ttu-id="9de93-132">GBV genera una salida de depuración después de que una llamada a [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) complete la ejecución en la GPU.</span><span class="sxs-lookup"><span data-stu-id="9de93-132">GBV produces debug output after a call to [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) completes execution on the GPU.</span></span> <span data-ttu-id="9de93-133">Dado que se encuentra en la escala de tiempo de GPU, la salida de depuración puede ser asincrónica con otra validación de la escala de tiempo de la CPU.</span><span class="sxs-lookup"><span data-stu-id="9de93-133">Since this is on the GPU-timeline the debug output may be asynchronous with other CPU-timeline validation.</span></span> <span data-ttu-id="9de93-134">Es posible que los desarrolladores de aplicaciones deseen inyectar su propio wait-After-Execute para sincronizar la salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="9de93-134">Application developers may want to inject their own wait-after-execute to synchronize debug output.</span></span>

<span data-ttu-id="9de93-135">La salida de GBV identifica dónde se produjo un error en un sombreador, junto con el recuento de Draw/envío actual y las identidades de los objetos relacionados (por ejemplo, lista de comandos, cola, PSO, etc.).</span><span class="sxs-lookup"><span data-stu-id="9de93-135">GBV output identifies where in a shader an error occurred, along with the current draw/dispatch count and identities of related objects (e.g. command list, queue, PSO, etc).</span></span>

## <a name="example-debug-message"></a><span data-ttu-id="9de93-136">Ejemplo de mensaje de depuración</span><span class="sxs-lookup"><span data-stu-id="9de93-136">Example debug message</span></span>

<span data-ttu-id="9de93-137">El siguiente mensaje de error indica que se ha tenido acceso a un recurso denominado "búfer de color principal" en un sombreador como un recurso de sombreador pero estaba en el estado de acceso desordenado cuando el sombreador se ejecutó en la GPU.</span><span class="sxs-lookup"><span data-stu-id="9de93-137">The following error message indicates that a resource named “Main Color Buffer” was accessed in a shader as a shader resource but was in the unordered access state when the shader ran on the GPU.</span></span> <span data-ttu-id="9de93-138">También se proporciona información adicional, como la ubicación en el origen del sombreador, el nombre de la lista de comandos y el recuento de Draw (dibujar índice), y los nombres de los objetos de interfaz D3D relacionados.</span><span class="sxs-lookup"><span data-stu-id="9de93-138">Additional information, such as the location in the shader source, the name of the command list and the Draw count (Draw Index), and the names of related D3D interface objects are also provided.</span></span>

```cmd
D3D12 ERROR: Incompatible resource state: Resource: 0x0000016F61A6EA80:'Main Color Buffer', 
Subresource Index: [0], 
Descriptor heap index: [0], 
Binding Type In Descriptor: SRV, 
Resource State: D3D12_RESOURCE_STATE_UNORDERED_ACCESS(0x8), 
Shader Stage: PIXEL, 
Root Parameter Index: [0], 
Draw Index: [0], 
Shader Code: E:\FileShare\MiniEngine_GitHub_160128\MiniEngine_GitHub\Core\Shaders\SharpeningUpsamplePS.hlsl(37,2-59), 
Asm Instruction Range: [0x138-0x16b], 
Asm Operand Index: [3], 
Command List: 0x0000016F6F75F740:'CommandList', SRV/UAV/CBV Descriptor Heap: 0x0000016F6F76F280:'Unnamed ID3D12DescriptorHeap Object', 
Sampler Descriptor Heap: <not set>, 
Pipeline State: 0x0000016F572C89F0:'Unnamed ID3D12PipelineState Object',  
[ EXECUTION ERROR #942: GPU_BASED_VALIDATION_INCOMPATIBLE_RESOURCE_STATE]
```

## <a name="debug-layer-apis"></a><span data-ttu-id="9de93-139">Depurar API de capa</span><span class="sxs-lookup"><span data-stu-id="9de93-139">Debug Layer APIs</span></span>

<span data-ttu-id="9de93-140">Para habilitar la capa de depuración, llame a [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span><span class="sxs-lookup"><span data-stu-id="9de93-140">To enable the debug layer, call [**EnableDebugLayer**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer).</span></span>

<span data-ttu-id="9de93-141">Para habilitar la validación basada en GPU, llame a [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation)y haga referencia a los métodos de las interfaces siguientes:</span><span class="sxs-lookup"><span data-stu-id="9de93-141">To enable GPU-based validation, call [**SetEnableGPUBasedValidation**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation), and refer to the methods of the following interfaces:</span></span>

- [<span data-ttu-id="9de93-142">**ID3D12Debug1**</span><span class="sxs-lookup"><span data-stu-id="9de93-142">**ID3D12Debug1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1)
- [<span data-ttu-id="9de93-143">**ID3D12DebugCommandList1**</span><span class="sxs-lookup"><span data-stu-id="9de93-143">**ID3D12DebugCommandList1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1)
- [<span data-ttu-id="9de93-144">**ID3D12DebugDevice1**</span><span class="sxs-lookup"><span data-stu-id="9de93-144">**ID3D12DebugDevice1**</span></span>](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1)

<span data-ttu-id="9de93-145">Consulte las siguientes enumeraciones y estructuras:</span><span class="sxs-lookup"><span data-stu-id="9de93-145">Refer to the following enumerations and structures:</span></span>

- [<span data-ttu-id="9de93-146">**\_Tipo de \_ parámetro de lista de comandos de depuración D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9de93-146">**D3D12\_DEBUG\_COMMAND\_LIST\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)
- [<span data-ttu-id="9de93-147">**\_Tipo de \_ parámetro de dispositivo de depuración D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9de93-147">**D3D12\_DEBUG\_DEVICE\_PARAMETER\_TYPE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)
- [<span data-ttu-id="9de93-148">**\_Estado de \_ canalización de validación basada en GPU D3D12 \_ \_ \_ \_ crear \_ marcas**</span><span class="sxs-lookup"><span data-stu-id="9de93-148">**D3D12\_GPU\_BASED\_VALIDATION\_PIPELINE\_STATE\_CREATE\_FLAGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)
- [<span data-ttu-id="9de93-149">**D3D12 \_ \_ modo de \_ \_ revisión del sombreador de validación basada \_ en GPU \_**</span><span class="sxs-lookup"><span data-stu-id="9de93-149">**D3D12\_GPU\_BASED\_VALIDATION\_SHADER\_PATCH\_MODE**</span></span>](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)
- [<span data-ttu-id="9de93-150">**D3D12 \_ depurar \_ \_ \_ configuración de \_ validación basada en GPU \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9de93-150">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)
- [<span data-ttu-id="9de93-151">**D3D12 \_ depurar \_ \_ \_ configuración de validación basada en GPU \_ del dispositivo \_**</span><span class="sxs-lookup"><span data-stu-id="9de93-151">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)

## <a name="related-topics"></a><span data-ttu-id="9de93-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9de93-152">Related topics</span></span>

* [<span data-ttu-id="9de93-153">Descripción de la capa de depuración de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9de93-153">Understanding the Direct3D 12 Debug Layer</span></span>](understanding-the-d3d12-debug-layer.md)
