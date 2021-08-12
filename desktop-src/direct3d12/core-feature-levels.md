---
title: Nivel de característica 12 Core 1.0 de Direct3D
description: El nivel de característica Core 1.0 es un subconjunto del conjunto completo de características de Direct3D 12.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 93eab39509074114bf2032cfb1cdea3e4e767dae9786241a34f970ca5cd51703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530725"
---
# <a name="the-direct3d-12-core-10-feature-level"></a>Nivel de característica 12 Core 1.0 de Direct3D

El nivel de característica Core 1.0 es un subconjunto del conjunto completo de características de Direct3D 12. El nivel de característica Core 1.0 se puede exponer mediante una categoría de dispositivos conocidos como *dispositivos de solo proceso.* El modelo de controlador general para dispositivos de solo proceso es El modelo de controlador de proceso de Microsoft (MCDM). MCDM es un par de escalado vertical del modelo Windows Device Driver Model (WDDM), que tiene un ámbito mayor.

Un dispositivo que solo *admite las* características de un nivel de característica principal se conoce como *dispositivo principal.*

> [!NOTE]
> *El dispositivo de solo proceso,* *el dispositivo MCDM,* el dispositivo *de nivel de* característica principal y el dispositivo *principal* significan lo mismo. Preferiremos el *dispositivo Core por* motivos de simplicidad.

## <a name="creating-a-core-device"></a>Creación de un dispositivo Core

En general, para crear un dispositivo Direct3D 12, llame a la función [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) y especifique un nivel de característica mínimo.

Si especifica un nivel de característica de 9 a 12, el dispositivo que se devuelve es un dispositivo con varias características, como una GPU tradicional (que admite un superconjunto de la funcionalidad de un dispositivo Core). Nunca se devuelve un dispositivo Core para ese intervalo de niveles de características.

Por otro lado, si especifica un nivel de característica Principal (por ejemplo, [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE),**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)el dispositivo que se devuelve podría tener muchas características o podría ser un dispositivo Core.

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

Si especifica un nivel de característica, la capa de tiempo de ejecución o depuración valida que las características que usa la aplicación están `_CORE` permitidas por ese `_CORE` nivel de característica. Ese conjunto de características se define más adelante en este tema.

## <a name="shader-model-for-core-devices"></a>Modelo de sombreador para dispositivos Principales

Un dispositivo Core admite Shader Model 5.0+.

El tiempo de ejecución realiza la conversión de modelos de sombreador 5.x que no son DXIL a DXIL 6.0. Por lo tanto, el controlador solo necesita admitir la versión 6.x.

## <a name="resource-management-model-for-core-devices"></a>Modelo de administración de recursos para dispositivos Principales

- Dimensiones de recursos admitidas: solo búferes sin procesar y estructurados (sin búferes con tipo, texture1d/2D, etc.)
- No se admiten recursos reservados (en mosaico)
- No se admiten montones personalizados
- No se admite ninguna de estas marcas de montón:
  - D3D12_HEAP_FLAG_HARDWARE_PROTECTED
  - D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH
  - D3D12_HEAP_FLAG_ALLOW_DISPLAY
  - D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (tenga en cuenta que los atomics del sombreador son necesarios, esta marca es para otra característica, los atomics del adaptador cruzado)

## <a name="resource-binding-model-for-core-devices"></a>Modelo de enlace de recursos para dispositivos Core

- Compatibilidad solo con el nivel 1 de enlace de recursos
- Excepciones:
  - No se admiten muestreadores de textura
  - Compatibilidad con 64 UAV como el nivel de característica 11.1+ (en lugar de solo 8)
  - Las implementaciones no tienen que implementar la comprobación de límites en los accesos del sombreador a los recursos a través de descriptores, los accesos fuera de límites generan un comportamiento indefinido.
    - Como producto secundario, no se admite la marca de intervalo D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS descriptor en las firmas raíz.
- Los descriptores UAV/CBV solo se pueden crear en recursos de montones predeterminados (por lo que no hay montones de carga o de lectura). Esto obliga a la aplicación a realizar copias para obtener datos a través de la CPU< de >GPU.
- A pesar de ser el nivel de funcionalidad de enlace más bajo, todavía hay algunas características necesarias incluso en este nivel que merece la pena mencionar:
  - Los montones de descriptores se pueden actualizar después de registrar las listas de comandos (consulte D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE en la especificación de enlace de recursos).
  - Los descriptores raíz son básicamente punteros GPUVA
    - Aunque no hay compatibilidad con MMU/VA, las VAs de búfer que se usan en descriptores raíz se pueden emular mediante implementaciones mediante la aplicación de revisiones de direcciones.

### <a name="structured-buffer-restrictions"></a>Restricciones de búfer estructurado

Los búferes estructurados deben tener una dirección base de 4 bytes alineada y el intervalo debe ser 2 o un múltiplo de 4. El caso de un paso de 2 es para las aplicaciones con datos de 16 bits, especialmente si no hay compatibilidad con búferes con tipo en D3D_FEATURE_LEVEL_1_0_CORE.

El intervalo especificado en los descriptores debe coincidir con el intervalo especificado en HLSL.  

## <a name="command-queue-support-for-core-devices"></a>Compatibilidad de la cola de comandos con dispositivos Core

Solo colas de proceso y copia (no colas 3D, vídeo, etc.).

## <a name="shader-support-for-core-devices"></a>Compatibilidad del sombreador con dispositivos Principales

Solo sombreadores de cálculo, ningún sombreador de gráficos (vértices, sombreadores de píxeles, etc.) ni ninguna funcionalidad relacionada, como destinos de representación, cadenas de intercambio, ensamblador de entrada.

### <a name="arithmetic-precision"></a>Precisión aritmética

Los dispositivos principales no tienen que admitir desnormas para operaciones de punto flotante de 16 bits.

## <a name="supported-apis-for-core-devices"></a>API admitidas para dispositivos principales

La lista siguiente representa el subconjunto admitido de la  interfaz de programación de aplicaciones completa  (no se muestran las API que no se admiten en el nivel de características core 1.0).

### <a name="id3d12device-methods"></a>Métodos ID3D12Device

* [ID3D12Device::CheckFeatureSupport](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [ID3D12Device::CopyDescriptors](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [ID3D12Device::CopyDescriptorsSimple](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [ID3D12Device::CreateCommandAllocator](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [ID3D12Device::CreateCommandList](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [ID3D12Device::CreateCommandQueue](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [ID3D12Device::CreateCommandSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [ID3D12Device::CreateCommittedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [ID3D12Device::CreateComputePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [ID3D12Device::CreateConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [ID3D12Device::CreateDescriptorHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [ID3D12Device::CreateFence](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [ID3D12Device::CreateHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [ID3D12Device::CreatePlacedResource](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [ID3D12Device::CreateQueryHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [ID3D12Device::CreateRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [ID3D12Device::CreateShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [ID3D12Device::CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [ID3D12Device::CreateUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [ID3D12Device::Evict](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [ID3D12Device::GetAdapterLuid](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [ID3D12Device::GetCopyableFootprints](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [ID3D12Device::GetCustomHeapProperties](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [ID3D12Device::GetDescriptorHandleIncrementSize](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [ID3D12Device::GetDeviceRemovedReason](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [ID3D12Device::GetNodeCount](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [ID3D12Device::GetResourceAllocationInfo](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [ID3D12Device::MakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [ID3D12Device::OpenSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [ID3D12Device::OpenSharedHandleByName](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [ID3D12Device::SetStablePowerState](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a>Métodos ID3D12Device1

* [ID3D12Device1::CreatePipelineLibrary](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [ID3D12Device1::SetEventOnMultipleFenceCompletion](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [ID3D12Device1::SetResidencySetEventOnMultipleFenceCompletionPriority](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a>Métodos ID3D12Device2

* [ID3D12Device2::CreatePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a>Métodos ID3D12Device3

* [ID3D12Device3::OpenExistingHeapFromAddress](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* [ID3D12Device3::OpenExistingHeapFromFileMapping](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))
* [ID3D12Device3::EnqueueMakeResident](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a>Métodos ID3D12Device4

* [ID3D12Device4::GetResourceAllocationInfo1](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a>Métodos ID3D12Device5

* [ID3D12Device5::CreateMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [ID3D12Device5::CreateStateObject](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [ID3D12Device5::EnumerateMetaCommandParameters](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [ID3D12Device5::EnumerateMetaCommands](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [ID3D12Device5::RemoveDevice](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a>Métodos ID3D12CommandQueue

* [ID3D12CommandQueue::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [ID3D12CommandQueue::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [ID3D12CommandQueue::ExecuteCommandLists](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [ID3D12CommandQueue::GetClock Yabration](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [ID3D12CommandQueue::GetDesc](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [ID3D12CommandQueue::GetTimestampFrequency](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [ID3D12CommandQueue::SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [ID3D12CommandQueue::Signal](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [ID3D12CommandQueue::Wait](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a>Métodos ID3D12CommandList

* [ID3D12CommandList::GetType](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a>Métodos ID3D12GraphicsCommandList

* [ID3D12GraphicsCommandList::BeginEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [ID3D12GraphicsCommandList::BeginQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [ID3D12GraphicsCommandList::ClearState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [ID3D12GraphicsCommandList::Close](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [ID3D12GraphicsCommandList::CopyBufferRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [ID3D12GraphicsCommandList::CopyResource](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [ID3D12GraphicsCommandList::CopyTextureRegion](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [ID3D12GraphicsCommandList::D ispatch](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [ID3D12GraphicsCommandList::EndEvent](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [ID3D12GraphicsCommandList::EndQuery](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [ID3D12GraphicsCommandList::Reset](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [ID3D12GraphicsCommandList::ResolveQueryData](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [ID3D12GraphicsCommandList::ResourceBartero](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstant](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstants](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [ID3D12GraphicsCommandList::SetComputeRootConstantBufferView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [ID3D12GraphicsCommandList::SetComputeRootDescriptorTable](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [ID3D12GraphicsCommandList::SetComputeRootShaderResourceView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [ID3D12GraphicsCommandList::SetComputeRootSignature](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [ID3D12GraphicsCommandList::SetDescriptorHeaps](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [ID3D12GraphicsCommandList::SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [ID3D12GraphicsCommandList::SetPipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [ID3D12GraphicsCommandList::SetPredication](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a>Métodos ID3D12GraphicsCommandList1

* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a>Métodos ID3D12GraphicsCommandList2

* [ID3D12GraphicsCommandList2::WriteBufferImmediate](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a>Métodos ID3D12GraphicsCommandList4

* [ID3D12GraphicsCommandList4::ExecuteMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [ID3D12GraphicsCommandList4::InitializeMetaCommand](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
