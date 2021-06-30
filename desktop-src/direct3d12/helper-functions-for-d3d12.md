---
title: Funciones auxiliares de D3D12
description: Estas funciones auxiliares ayudan especialmente a controlar los subrecursos y se declaran en d3dx12.h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funciones auxiliares
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10736d91da0e2c4efa2a3c981ab5c4f64e2af86d
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102143"
---
# <a name="helper-functions-for-d3d12"></a><span data-ttu-id="5cf57-105">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="5cf57-105">Helper Functions for D3D12</span></span>

<span data-ttu-id="5cf57-106">Estas funciones auxiliares ayudan especialmente a controlar los subrecursos y se declaran en **d3dx12.h**.</span><span class="sxs-lookup"><span data-stu-id="5cf57-106">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5cf57-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5cf57-107">In this section</span></span>



| <span data-ttu-id="5cf57-108">Tema</span><span class="sxs-lookup"><span data-stu-id="5cf57-108">Topic</span></span>                                                                                             | <span data-ttu-id="5cf57-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cf57-109">Description</span></span>                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cf57-110">**CommandListCast**</span><span class="sxs-lookup"><span data-stu-id="5cf57-110">**CommandListCast**</span></span>](commandlistcast.md)<br/>                                     | <span data-ttu-id="5cf57-111">Esta plantilla de función convierte un puntero constante a cualquier lista de comandos en un puntero const a id3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="5cf57-111">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="5cf57-112">**D3D12CalcSubresource**</span><span class="sxs-lookup"><span data-stu-id="5cf57-112">**D3D12CalcSubresource**</span></span>](d3d12calcsubresource.md)<br/>                                   | <span data-ttu-id="5cf57-113">Calcula un índice de subrecurso para una textura.</span><span class="sxs-lookup"><span data-stu-id="5cf57-113">Calculates a subresource index for a texture.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="5cf57-114">**D3D12DecomposeSubresource**</span><span class="sxs-lookup"><span data-stu-id="5cf57-114">**D3D12DecomposeSubresource**</span></span>](d3d12decomposesubresource.md)<br/>                         | <span data-ttu-id="5cf57-115">Genera el segmento mip, el segmento de matriz y el segmento de plano que corresponden al índice de subrecurso especificado.</span><span class="sxs-lookup"><span data-stu-id="5cf57-115">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span> <br/>                                                                                                                                        |
| [<span data-ttu-id="5cf57-116">**D3D12GetFormatPlaneCount**</span><span class="sxs-lookup"><span data-stu-id="5cf57-116">**D3D12GetFormatPlaneCount**</span></span>](d3d12getformatplanecount.md)<br/>                           | <span data-ttu-id="5cf57-117">Obtiene el número de planos para el formato DXGI especificado para el adaptador virtual especificado **(id. 3D12Device).**</span><span class="sxs-lookup"><span data-stu-id="5cf57-117">Gets the number of planes for the specified DXGI format for the specified virtual adapter (an **ID3D12Device**).</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="5cf57-118">**D3D12IsLayoutOpaque**</span><span class="sxs-lookup"><span data-stu-id="5cf57-118">**D3D12IsLayoutOpaque**</span></span>](d3d12islayoutopaque.md)<br/>                                     | <span data-ttu-id="5cf57-119">Indica si el diseño es opaco.</span><span class="sxs-lookup"><span data-stu-id="5cf57-119">Indicates whether the layout is opaque.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="5cf57-120">**D3DX12GetBaseSubobjectType**</span><span class="sxs-lookup"><span data-stu-id="5cf57-120">**D3DX12GetBaseSubobjectType**</span></span>](d3dx12getbasesubobjecttype.md)<br/>                       | <span data-ttu-id="5cf57-121">Devuelve el tipo de subobjeto que corresponde a la clase base del tipo de subobjeto pasado.</span><span class="sxs-lookup"><span data-stu-id="5cf57-121">Returns the subobject type that corresponds to the base class of the passed-in subobject type.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="5cf57-122">**D3DX12ParsePipelineStateStream**</span><span class="sxs-lookup"><span data-stu-id="5cf57-122">**D3DX12ParsePipelineStateStream**</span></span>](d3dx12parsepipelinestream.md)<br/>                    | <span data-ttu-id="5cf57-123">Analiza una descripción de flujo de estado de canalización, llamando a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.</span><span class="sxs-lookup"><span data-stu-id="5cf57-123">Parses a pipeline state stream description, calling a user-defined callback for each subobject instance parsed.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="5cf57-124">**D3DX12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5cf57-124">**D3DX12SerializeVersionedRootSignature**</span></span>](d3dx12serializeversionedrootsignature.md)<br/> | <span data-ttu-id="5cf57-125">Ayuda a habilitar las características de firma raíz 1.1 cuando están disponibles y no requiere mantener dos rutas de acceso de código para crear firmas raíz.</span><span class="sxs-lookup"><span data-stu-id="5cf57-125">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="5cf57-126">Este método auxiliar reconstruye una firma raíz de la versión 1.0 cuando no se admite la versión 1.1.</span><span class="sxs-lookup"><span data-stu-id="5cf57-126">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span><br/> |
| [<span data-ttu-id="5cf57-127">**GetRequiredIntermediateSize**</span><span class="sxs-lookup"><span data-stu-id="5cf57-127">**GetRequiredIntermediateSize**</span></span>](getrequiredintermediatesize.md)<br/>                     | <span data-ttu-id="5cf57-128">Devuelve el tamaño necesario de un búfer que se va a usar para la carga de datos.</span><span class="sxs-lookup"><span data-stu-id="5cf57-128">Returns the required size of a buffer to be used for data upload.</span></span> <br/>                                                                                                                                                                              |
| [<span data-ttu-id="5cf57-129">**Memcpysubresource**</span><span class="sxs-lookup"><span data-stu-id="5cf57-129">**Memcpysubresource**</span></span>](memcpysubresource.md)<br/>                                         | <span data-ttu-id="5cf57-130">Copia una fila de subrecurso por fila.</span><span class="sxs-lookup"><span data-stu-id="5cf57-130">Copies a subresource row by row.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="5cf57-131">**Updatesubresources**</span><span class="sxs-lookup"><span data-stu-id="5cf57-131">**Updatesubresources**</span></span>](updatesubresources1.md)<br/>                                      | <span data-ttu-id="5cf57-132">Actualiza los subrecursos, todas las matrices de subrecursos deben rellenarse, normalmente llamando a [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="5cf57-132">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span> <br/>                                                                  |
| [<span data-ttu-id="5cf57-133">**Updatesubresources (asignación de montones)**</span><span class="sxs-lookup"><span data-stu-id="5cf57-133">**Updatesubresources (heap-allocating)**</span></span>](updatesubresources2.md)<br/>                    | <span data-ttu-id="5cf57-134">Actualiza los subrecursos con una implementación de asignación de montón.</span><span class="sxs-lookup"><span data-stu-id="5cf57-134">Updates subresources with a heap-allocating implementation.</span></span> <br/>                                                                                                                                                                                    |
| [<span data-ttu-id="5cf57-135">**Updatesubresources (asignación de pila)**</span><span class="sxs-lookup"><span data-stu-id="5cf57-135">**Updatesubresources (stack-allocating)**</span></span>](updatesubresources3.md)<br/>                   | <span data-ttu-id="5cf57-136">Actualiza los subrecursos con una implementación de asignación de pila.</span><span class="sxs-lookup"><span data-stu-id="5cf57-136">Updates subresources with a stack-allocating implementation.</span></span> <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="5cf57-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5cf57-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cf57-138">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5cf57-138">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="5cf57-139">Estructuras y funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="5cf57-139">Helper Structures and Functions for D3D12</span></span>](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





