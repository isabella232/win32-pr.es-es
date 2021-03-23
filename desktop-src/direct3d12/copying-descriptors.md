---
title: Descriptores de copias
description: Los métodos ID3D12Device CopyDescriptors y ID3D12Device CopyDescriptorsSimple en la interfaz de dispositivo usan la CPU para copiar descriptores inmediatamente.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104510"
---
# <a name="copying-descriptors"></a><span data-ttu-id="c53d0-103">Descriptores de copias</span><span class="sxs-lookup"><span data-stu-id="c53d0-103">Copying Descriptors</span></span>

<span data-ttu-id="c53d0-104">Los métodos [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) y [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) de la interfaz de dispositivo usan la CPU para copiar descriptores inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c53d0-104">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="c53d0-105">Se puede llamar subprocesamiento libre siempre que varios subprocesos de la CPU o GPU no realicen ninguna escritura en conflicto.</span><span class="sxs-lookup"><span data-stu-id="c53d0-105">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span>

## <a name="copying-descriptors-immediately-cpu-timeline"></a><span data-ttu-id="c53d0-106">Copia de descriptores inmediatamente (escala de tiempo de CPU)</span><span class="sxs-lookup"><span data-stu-id="c53d0-106">Copying Descriptors Immediately (CPU Timeline)</span></span>

<span data-ttu-id="c53d0-107">El número de descriptores de origen (de los que se copia), especificado como un conjunto de intervalos de descriptor, debe ser igual al número de descriptores de destino (para copiar en), especificado como un conjunto independiente de intervalos de descriptor.</span><span class="sxs-lookup"><span data-stu-id="c53d0-107">The number of source descriptors (to copy from), specified as a set of descriptor ranges, must equal the number of destination descriptors (to copy to), specified as a separate set of descriptor ranges.</span></span> <span data-ttu-id="c53d0-108">De lo contrario, los intervalos de origen y destino no tienen que alinearse.</span><span class="sxs-lookup"><span data-stu-id="c53d0-108">The source and destination ranges do not otherwise have to line up.</span></span> <span data-ttu-id="c53d0-109">Por ejemplo, un conjunto de descriptores dispersos podría copiarse en un destino contiguo, viceversa o en alguna combinación.</span><span class="sxs-lookup"><span data-stu-id="c53d0-109">For example, a sparse set of descriptors could be copied to a contiguous destination, vice versa, or in some combination.</span></span>

<span data-ttu-id="c53d0-110">En la operación de copia pueden participar varios montones de descriptor, como origen y destino.</span><span class="sxs-lookup"><span data-stu-id="c53d0-110">Multiple descriptor heaps can be involved in the copy operation, both as source and destination.</span></span> <span data-ttu-id="c53d0-111">El uso de identificadores de descriptor como parámetros significa que los métodos de copia no están relacionados con los montones en los que se encuentra ningún descriptor determinado, sino que son solo memoria.</span><span class="sxs-lookup"><span data-stu-id="c53d0-111">The use of descriptor handles as parameters means the copy methods don’t care about which heaps any given descriptor lies in – they are all just memory.</span></span>

<span data-ttu-id="c53d0-112">Los tipos del montón descriptor que se copian de y a deben coincidir, por lo que los métodos toman un único tipo de montón de descriptor como entrada.</span><span class="sxs-lookup"><span data-stu-id="c53d0-112">The descriptor heap types being copied from and to must match, so the methods take a single descriptor heap type as input.</span></span> <span data-ttu-id="c53d0-113">El controlador debe conocer el tipo de montón de todos los descriptores de la operación de copia dada, por lo que sabe qué tamaño de los datos están implicados en la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="c53d0-113">The driver needs to know the heap type of all the descriptors in the given copy operation, so it knows what size of data is involved in the copy operation.</span></span> <span data-ttu-id="c53d0-114">Es posible que el controlador también tenga que realizar trabajos de copia personalizados si un determinado tipo de montón de descriptores lo justifica: un detalle de implementación.</span><span class="sxs-lookup"><span data-stu-id="c53d0-114">The driver might also need to do custom copying work if a given descriptor heap type warrants it – an implementation detail.</span></span> <span data-ttu-id="c53d0-115">Tenga en cuenta que, en caso contrario, los controladores de descriptores no identifican el tipo al que apuntan. por lo tanto, se requiere un parámetro adicional para la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="c53d0-115">Note that descriptor handles themselves do not otherwise identify what type they are pointing to; therefore, an additional parameter is required for the copy operation.</span></span>

<span data-ttu-id="c53d0-116">Se proporciona una API alternativa a [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) para el caso simple de copiar un único intervalo de descriptores de una ubicación a otra – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span><span class="sxs-lookup"><span data-stu-id="c53d0-116">An alternative API to [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) is provided for the simple case of copying a single range of descriptors from one location to another – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span></span>

<span data-ttu-id="c53d0-117">Para estos métodos de copia de descriptores basados en dispositivos (escala de tiempo de CPU), los descriptores de origen deben provienen de un montón de descriptor visible sin sombreador.</span><span class="sxs-lookup"><span data-stu-id="c53d0-117">For these device based (CPU timeline) descriptor copy methods, source descriptors must come from a non-shader visible descriptor heap.</span></span> <span data-ttu-id="c53d0-118">Los descriptores de destino pueden estar en cualquier montón de descriptores que esté visible en la CPU (sombreador visible o no).</span><span class="sxs-lookup"><span data-stu-id="c53d0-118">The destination descriptors can be in any descriptor heap that is CPU visible (shader visible or not).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c53d0-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c53d0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c53d0-120">Descriptores de</span><span class="sxs-lookup"><span data-stu-id="c53d0-120">Descriptors</span></span>](descriptors.md)
</dt> </dl>

 

 




