---
title: Descriptores de
description: Los descriptores son la unidad principal de enlace para un único recurso de D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104093"
---
# <a name="descriptors"></a><span data-ttu-id="1b740-103">Descriptores de</span><span class="sxs-lookup"><span data-stu-id="1b740-103">Descriptors</span></span>

<span data-ttu-id="1b740-104">Los descriptores son la unidad principal de enlace para un único recurso de D3D12.</span><span class="sxs-lookup"><span data-stu-id="1b740-104">Descriptors are the primary unit of binding for a single resource in D3D12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1b740-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1b740-105">In this section</span></span>



| <span data-ttu-id="1b740-106">Tema</span><span class="sxs-lookup"><span data-stu-id="1b740-106">Topic</span></span>                                                       | <span data-ttu-id="1b740-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b740-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1b740-108">Información general sobre descriptores</span><span class="sxs-lookup"><span data-stu-id="1b740-108">Descriptors Overview</span></span>](descriptors-overview.md)<br/> | <span data-ttu-id="1b740-109">Los descriptores se crean mediante llamadas API e identifican recursos.</span><span class="sxs-lookup"><span data-stu-id="1b740-109">Descriptors are created by API calls and identify resources.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="1b740-110">Crear descriptores</span><span class="sxs-lookup"><span data-stu-id="1b740-110">Creating Descriptors</span></span>](creating-descriptors.md)<br/> | <span data-ttu-id="1b740-111">Describe y muestra ejemplos para crear vistas de búfer de índice, vértices y constantes; recursos del sombreador, destino de representación, acceso desordenado, salida de secuencia y vistas de la galería de símbolos de profundidad; y muestreadores.</span><span class="sxs-lookup"><span data-stu-id="1b740-111">Describes and shows examples for creating index, vertex, and constant buffer views; shader resource, render target, unordered access, stream output and depth-stencil views; and samplers.</span></span> <span data-ttu-id="1b740-112">Todos los métodos para crear descriptores son de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="1b740-112">All methods for creating descriptors are free threaded.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="1b740-113">Descriptores de copias</span><span class="sxs-lookup"><span data-stu-id="1b740-113">Copying Descriptors</span></span>](copying-descriptors.md)<br/>   | <span data-ttu-id="1b740-114">Los métodos [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) y [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) de la interfaz de dispositivo usan la CPU para copiar descriptores inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="1b740-114">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="1b740-115">Se puede llamar subprocesamiento libre siempre que varios subprocesos de la CPU o GPU no realicen ninguna escritura en conflicto.</span><span class="sxs-lookup"><span data-stu-id="1b740-115">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1b740-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1b740-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b740-117">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="1b740-117">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="1b740-118">Tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="1b740-118">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> <dt>

[<span data-ttu-id="1b740-119">Enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="1b740-119">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="1b740-120">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="1b740-120">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 





