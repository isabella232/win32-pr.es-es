---
title: Sistemas de varios adaptadores
description: Describe la compatibilidad con Direct3D 12 para sistemas que tienen varios adaptadores instalados, que abarca escenarios donde la aplicación tiene como destino explícita varios adaptadores de GPU y escenarios en los que los controladores usan implícitamente varios adaptadores de GPU en nombre de la aplicación.
ms.assetid: CC4C6594-D48F-40C1-93EE-9F98532BC038
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: e76c5c1295dab8858ff04830030efb479fe3ae8a09bcdb37ff8c4820f4fd08c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728825"
---
# <a name="multi-adapter-systems"></a>Sistemas de varios adaptadores

Describe la compatibilidad con Direct3D 12 para sistemas que tienen varios adaptadores instalados, que abarca escenarios donde la aplicación tiene como destino explícita varios adaptadores de GPU y escenarios en los que los controladores usan implícitamente varios adaptadores de GPU en nombre de la aplicación.

## <a name="multi-adapter-overview"></a>Información general sobre varios adaptadores

Un adaptador de GPU puede ser cualquier adaptador (gráficos o proceso, discreto o integrado) de cualquier fabricante que admita Direct3D 12.

Se hace referencia a varios adaptadores como *nodos*. Varios elementos, como las colas, se aplican a cada nodo, por lo que si hay dos nodos, habrá dos colas 3D predeterminadas. Otros elementos, como el estado de canalización y las firmas raíz y de comando, pueden hacer referencia a uno o varios nodos o a todos, como se muestra en el diagrama.

![las colas se aplican a cada adaptador de gráficos](images/multigpu.png)

## <a name="sharing-heaps-across-adapters"></a>Uso compartido de montones entre adaptadores

Consulte el [tema Montones compartidos.](shared-heaps.md)

## <a name="multi-adapter-apis-and-node-masks"></a>API de varios adaptadores y máscaras de nodo

De forma similar a las API anteriores de Direct3D, cada conjunto de adaptadores vinculados se enumera como un único [**objeto IDXGIAdapter3.**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) Todas las salidas asociadas a cualquier adaptador del vínculo se enumeran como adjuntas al único **objeto IDXGIAdapter3.**

La aplicación puede determinar el número de adaptadores físicos asociados a un dispositivo determinado llamando a [**ID3D12Device::GetNodeCount**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount).

Muchas API de Direct3D 12 aceptan una máscara de nodo *(una* máscara de bits), que indica el conjunto de nodos a los que hace referencia la llamada API. Cada nodo tiene un índice de base cero. Pero en la máscara de nodo, cero se traduce en el bit 1; 1 se traduce en el bit 2; y así sucesivamente.

### <a name="single-nodes"></a>Nodos únicos

Al llamar a las siguientes API (nodo único), la aplicación especifica un único nodo al que se asociará la llamada API. La mayoría de las veces, esto se especifica mediante una máscara de nodo. Cada bit de la máscara corresponde a un único nodo. Para todas las API descritas en esta sección, debe establecer exactamente un bit en la máscara de nodo.

-   [**D3D12 \_ COMMAND \_ QUEUE \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) tiene un *miembro NodeMask.*
-   [**CreateCommandQueue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) crea una cola a partir de una estructura [**\_ \_ \_ DESC COMMAND QUEUE de D3D12.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)
-   [**CreateCommandList:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) toma un *parámetro nodeMask.*
-   [**D3D12 \_ DESCRIPTOR \_ HEAP \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) tiene un *miembro NodeMask.*
-   [**CreateDescriptorHeap:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap) crea un montón de descriptores a partir de una estructura [**\_ \_ \_ DESC HEAP del DESCRIPTOR D3D12.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)
-   [**D3D12 \_ QUERY \_ HEAP \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc) tiene un *miembro NodeMask.*
-   [**CreateQueryHeap:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap) crea un montón de consultas a partir de una estructura [**D3D12 \_ QUERY \_ HEAP \_ DESC.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_query_heap_desc)

### <a name="multiple-nodes"></a>Varios nodos

Al llamar a las siguientes API (varios nodos), la aplicación especifica un conjunto de nodos a los que se asociará la llamada API. La afinidad de nodo se especifica como una máscara de nodo, posiblemente con varios bits establecidos. Si la aplicación pasa 0 para esta máscara de bits, el controlador Direct3D 12 lo convierte en la máscara de bits 1 (lo que indica que el objeto está asociado al nodo 0).

-   [**D3D12 \_ CROSS \_ NODE SHARING TIER \_ \_ :**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier) determina la compatibilidad con el uso compartido entre nodos.
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : estructura que hace referencia a [**D3D12 \_ CROSS NODE SHARING \_ \_ \_ TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_cross_node_sharing_tier).
-   [**D3D12 \_ FEATURE \_ DATA \_ ARCHITECTURE:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) contiene un *miembro NodeIndex.*
-   [**D3D12 \_ DESC DE ESTADO DE CANALIZACIÓN \_ \_ DE \_ GRÁFICOS:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) tiene un *miembro NodeMask.*
-   [**CreateGraphicsPipelineState:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) crea un objeto de estado de canalización de gráficos a partir de una estructura [**\_ \_ \_ \_ DESC GRAPHICS PIPELINE STATE de D3D12.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)
-   [**D3D12 \_ COMPUTE \_ PIPELINE \_ STATE \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc) tiene un *miembro NodeMask.*
-   [**CreateComputePipelineState:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) crea un objeto de estado de canalización de proceso a partir de una estructura [**\_ \_ \_ \_ DESC COMPUTE PIPELINE STATE de D3D12.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc)
-   [**CreateRootSignature:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)toma un *parámetro nodeMask.*
-   [**D3D12 \_ COMMAND \_ SIGNATURE \_ DESC:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc)tiene un *miembro NodeMask.*
-   [**CreateCommandSignature:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) crea un objeto de firma de comando a partir de una estructura [**\_ \_ \_ DESC COMMAND SIGNATURE de D3D12.**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

### <a name="resource-creation-apis"></a>API de creación de recursos

Las siguientes API hacen referencia a máscaras de nodo.

-   [**D3D12 \_ PROPIEDADES DEL \_ MONTÓN:**](/windows/win32/api/d3d12/ns-d3d12-d3d12_heap_properties) tiene miembros *CreationNodeMask* y *VisibleNodeMask.*
-   [**GetResourceAllocationInfo:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) tiene un *parámetro visibleMask.*
-   [**GetCustomHeapProperties:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties) tiene un *parámetro nodeMask.*

Al crear un recurso reservado, no se especifica ningún índice de nodo ni máscara. El recurso reservado se puede asignar a un montón en cualquier nodo (siguiendo las reglas de uso compartido entre nodos).

El método [**MakeResident**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident) funciona internamente con colas de adaptador; no es necesario que la aplicación especifique nada para esto.

Al llamar a las siguientes API [**ID3D12Device,**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) la aplicación no necesita especificar un conjunto de nodos a los que se asociará la llamada API porque la llamada API se aplica a todos los nodos.

-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
-   [**GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
-   [**SetStablePowerState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
-   [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
-   [**CreateSampler**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsampler)
-   [**CopyDescriptors**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
-   [**CopyDescriptorsSimple**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
-   [**CreateSharedHandle**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
-   [**OpenSharedHandleByName**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
-   [**OpenSharedHandle:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle) con una *barrera* como parámetro. Con un recurso  *o* un montón como parámetros, este método no acepta nodos como parámetros porque las máscaras de nodo se heredan de objetos creados anteriormente.
-   [**CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
-   [**CreateConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
-   [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)
-   [**CreateUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
-   [**CreateDepthStencilView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdepthstencilview)
-   [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)

## <a name="related-topics"></a>Temas relacionados

[Guía de programación de Direct3D 12](directx-12-programming-guide.md)