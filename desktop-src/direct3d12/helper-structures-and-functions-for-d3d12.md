---
title: Estructuras y funciones auxiliares de D3D12
description: Estas estructuras auxiliares y funciones auxiliares se declaran en d3dx12. h.
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Funciones auxiliares
- Estructuras auxiliares
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d612d97610a749f32a6a23010b632c17d34461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105720081"
---
# <a name="helper-structures-and-functions-for-d3d12"></a><span data-ttu-id="d4fe9-106">Estructuras y funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="d4fe9-106">Helper Structures and Functions for D3D12</span></span>

<span data-ttu-id="d4fe9-107">Estas estructuras auxiliares y funciones auxiliares se declaran en **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="d4fe9-107">These helper structures and helper functions are declared in **d3dx12.h**.</span></span>

<span data-ttu-id="d4fe9-108">Puede usar estas estructuras auxiliares para crear e inicializar estructuras de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d4fe9-108">You can use these helper structures to create and initialize Direct3D structures.</span></span> <span data-ttu-id="d4fe9-109">Estas estructuras auxiliares se comportan como clases de C++.</span><span class="sxs-lookup"><span data-stu-id="d4fe9-109">These helper structures behave like C++ classes.</span></span> <span data-ttu-id="d4fe9-110">Cada estructura de aplicación auxiliar tiene normalmente un constructor predeterminado, un constructor explícito, un destructor y un operador de conversión para la estructura D3D12 asociada.</span><span class="sxs-lookup"><span data-stu-id="d4fe9-110">Each helper structure typically has a default constructor, an explicit constructor, a destructor, and a cast operator for the associated D3D12 structure.</span></span> <span data-ttu-id="d4fe9-111">Cada estructura auxiliar tiene un prefijo "C" y está asociada a una estructura D3D12 que carece del prefijo "C".</span><span class="sxs-lookup"><span data-stu-id="d4fe9-111">Each helper structure has a 'C' prefix and is associated with a D3D12 structure which lacks the 'C' prefix.</span></span> <span data-ttu-id="d4fe9-112">La mayoría de las estructuras auxiliares contienen métodos de miembro de inicialización, algunos contienen funciones de comparación.</span><span class="sxs-lookup"><span data-stu-id="d4fe9-112">Most helper structures contain initialization member methods, some contain comparison functions.</span></span>

<span data-ttu-id="d4fe9-113">**d3dx12. h** está disponible por separado de los encabezados de Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="d4fe9-113">**d3dx12.h** is available separately from the Direct3D 12 headers.</span></span> <span data-ttu-id="d4fe9-114">Puede descargar **d3dx12. h** desde [la biblioteca auxiliar de D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span><span class="sxs-lookup"><span data-stu-id="d4fe9-114">You can download **d3dx12.h** from [The D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4fe9-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="d4fe9-115">In this section</span></span>



| <span data-ttu-id="d4fe9-116">Tema</span><span class="sxs-lookup"><span data-stu-id="d4fe9-116">Topic</span></span>                                                                     | <span data-ttu-id="d4fe9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4fe9-117">Description</span></span>                                                                                                              |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4fe9-118">Interfaces auxiliares para D3D12</span><span class="sxs-lookup"><span data-stu-id="d4fe9-118">Helper Interfaces for D3D12</span></span>](helper-interfaces-for-d3d12.md)<br/> | <span data-ttu-id="d4fe9-119">Estas interfaces auxiliares ayudan especialmente en el control de Subrecursos y se declaran en **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="d4fe9-119">These helper interfaces help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>        |
| [<span data-ttu-id="d4fe9-120">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="d4fe9-120">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)<br/> | <span data-ttu-id="d4fe9-121">Estas estructuras auxiliares ayudan a inicializar muchas de las estructuras de Direct3D 12 y se declaran en **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="d4fe9-121">These helper structures help initialize many of the Direct3D 12 structures, and are declared in **d3dx12.h**.</span></span><br/> |
| [<span data-ttu-id="d4fe9-122">Funciones auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="d4fe9-122">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)<br/>   | <span data-ttu-id="d4fe9-123">Estas funciones auxiliares ayudan especialmente en el control de Subrecursos y se declaran en **d3dx12. h**.</span><span class="sxs-lookup"><span data-stu-id="d4fe9-123">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d4fe9-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4fe9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4fe9-125">Referencia de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="d4fe9-125">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





