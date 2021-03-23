---
title: Sistemas de varios adaptadores
description: Describe la compatibilidad en Direct3D 12 para sistemas que tienen instalados varios adaptadores, que abarcan escenarios en los que la aplicación tiene como destino explícitamente varios adaptadores de GPU y escenarios en los que los controladores usan implícitamente varios adaptadores de GPU en nombre de la aplicación.
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d7d3985c880c4d1732a96b98ac6d3c6579dab8e6
ms.sourcegitcommit: 9d530b0a2396f2274e9ed693c1f5f10556aadebb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/09/2020
ms.locfileid: "104549079"
---
# <a name="multi-adapter-systems"></a>Sistemas de varios adaptadores

Describe la compatibilidad en Direct3D 12 para sistemas que tienen instalados varios adaptadores, que abarcan escenarios en los que la aplicación tiene como destino explícitamente varios adaptadores de GPU y escenarios en los que los controladores usan implícitamente varios adaptadores de GPU en nombre de la aplicación.

## <a name="multi-adapter-overview"></a>Información general de varios adaptadores

Un adaptador de GPU puede ser cualquier adaptador (gráficos o proceso, discreto o integrado), de cualquier fabricante, que admita Direct3D 12.

Se hace referencia a varios adaptadores como *nodos*. Varios elementos, como las colas, se aplican a cada nodo, por lo que si hay dos nodos, habrá dos colas 3D predeterminadas. Otros elementos, como el estado de la canalización y las firmas de comando y raíz, pueden hacer referencia a uno o varios de los nodos, tal y como se muestra en el diagrama.

![las colas se aplican a cada adaptador de gráficos](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>Uso compartido de montones entre adaptadores

Vea el tema sobre [montones compartidos](shared-heaps.md) .

## <a name="multi-adapter-apis-and-node-masks"></a>API de varios adaptadores y máscaras de nodo

De forma similar a las API de Direct3D anteriores, cada conjunto de adaptadores vinculados se enumera como un solo objeto [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) . Todas las salidas asociadas a cualquier adaptador del vínculo se enumeran como adjuntas al único objeto **IDXGIAdapter3** .

La aplicación puede determinar el número de adaptadores físicos asociados a un determinado dispositivo mediante una llamada a [**ID3D12Device:: GetNodeCount**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount).

Muchas API de Direct3D 12 aceptan una *máscara de nodo* (máscara de bits), que indica el conjunto de nodos a los que hace referencia la llamada API. Cada nodo tiene un índice basado en cero. Pero en la máscara de nodo, cero se traduce en el bit 1; 1 se traduce en el bit 2; etc.

### <a name="single-nodes"></a>Nodos únicos

Al llamar a las siguientes API (nodo único), la aplicación especifica un único nodo con el que se asociará la llamada a la API. La mayoría de las veces, esto se especifica mediante una máscara de nodo. Cada bit de la máscara corresponde a un solo nodo. Para todas las API descritas en esta sección, debe establecer exactamente un bit en la máscara de nodo.

-   [**D3D12 \_ La \_ cola \_ de comandos DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) : tiene un miembro *NodeMask* .
-   [**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) : crea una cola a partir de una estructura de DESC de la [**\_ cola de comandos de \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) .
-   [**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) : toma un parámetro *nodeMask* .
-   [**D3D12 \_ Descriptor \_ heap \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) : tiene un miembro *NodeMask* .
-   [**CreateDescriptorHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) : crea un montón de descriptores a partir de una estructura de [**\_ \_ \_ DESC del descriptor de D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) .
-   [**D3D12 \_ Montón de consulta \_ \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) : tiene un miembro *NodeMask* .
-   [**CreateQueryHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) : crea un montón de consulta a partir de una estructura de [**\_ DESC del \_ montón \_ de consulta D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) .

### <a name="multiple-nodes"></a>Varios nodos

Al llamar a las siguientes API (varios nodos), la aplicación especifica un conjunto de nodos a los que se asociará la llamada API. La afinidad de nodo se especifica como una máscara de nodo, potencialmente con varios bits establecidos. Si la aplicación pasa 0 para esta máscara de bits, el controlador de Direct3D 12 la convierte en la máscara de bits 1 (lo que indica que el objeto está asociado al nodo 0).

-   [**D3D12 \_ \_Nivel de \_ uso \_ compartido entre nodos**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) : determina la compatibilidad con el uso compartido entre nodos.
-   [**D3D12 \_ \_Opciones de \_ D3D12 \_ de datos de características**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : estructura que hace referencia al [**\_ \_ \_ \_ nivel de uso compartido entre nodos D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier).
-   [**D3D12 \_ \_ \_ Arquitectura de datos de características**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) : contiene un miembro *NodeIndex* .
-   [**D3D12 \_ \_Estado de canalización de gráficos \_ \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) : tiene un miembro *NodeMask* .
-   [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) : crea un objeto de estado de canalización de gráficos a partir de una estructura de [**\_ DESC de \_ \_ estado \_ de canalización D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) .
-   [**D3D12 \_ Estado de \_ canalización de proceso \_ \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) : tiene un miembro *NodeMask* .
-   [**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) : crea un objeto de estado de canalización de proceso a partir de una estructura de [**\_ DESC de \_ \_ estado \_ de canalización de proceso D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) .
-   [**CreateRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature): toma un parámetro *nodeMask* .
-   [**D3D12 \_ La \_ firma \_ del comando DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc): tiene un miembro *NodeMask* .
-   [**CreateCommandSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) : crea un objeto de firma de comando a partir de una estructura de DESC de la [**\_ firma del comando \_ \_ D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc) .

### <a name="resource-creation-apis"></a>API de creación de recursos

Las siguientes API hacen referencia a las máscaras de nodo.

-   [**D3D12 \_ \_Propiedades del montón**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) : tiene los miembros *CreationNodeMask* y *VisibleNodeMask* .
-   [**GetResourceAllocationInfo**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) : tiene un parámetro *visibleMask* .
-   [**GetCustomHeapProperties**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) : tiene un parámetro *nodeMask* .

Al crear un recurso reservado, no se especifica ningún índice de nodo ni máscara. El recurso reservado se puede asignar a un montón en cualquier nodo (según las reglas de uso compartido entre nodos).

El método [**MakeResident**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) funciona internamente con las colas del adaptador; no es necesario que la aplicación especifique nada para ello.

Cuando se llama a las siguientes API de [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) , la aplicación no tiene que especificar un conjunto de nodos al que se asociará la llamada API porque la llamada a la API se aplica a todos los nodos.

-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**CreateSampler**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**OpenSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) : con una *barrera* como parámetro. Con un *recurso* o un *montón* como parámetros, este método no acepta nodos como parámetros porque las máscaras de nodo se heredan de los objetos creados anteriormente.
-   [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**CreateUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**CreateDepthStencilView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>Temas relacionados

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)