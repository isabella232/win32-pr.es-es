---
title: Usar constantes directamente en la firma raíz
description: Las aplicaciones pueden definir constantes raíz en la firma raíz, cada una como un conjunto de valores de 32 bits. Aparecen en el lenguaje de sombreado de alto nivel (HLSL) como un búfer de constantes. Tenga en cuenta que los búferes de constantes para las razones históricas se ven como conjuntos de valores de 4x32 bits.
ms.assetid: F9A2640F-D1FA-481C-BDF1-B15372E3C512
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3cd3980bede72d6e2f4b163abe11b249970eb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104676"
---
# <a name="using-constants-directly-in-the-root-signature"></a><span data-ttu-id="4221f-105">Usar constantes directamente en la firma raíz</span><span class="sxs-lookup"><span data-stu-id="4221f-105">Using Constants Directly in the Root Signature</span></span>

<span data-ttu-id="4221f-106">Las aplicaciones pueden definir constantes raíz en la firma raíz, cada una como un conjunto de valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4221f-106">Applications can define root constants in the root signature, each as a set of 32-bit values.</span></span> <span data-ttu-id="4221f-107">Aparecen en el lenguaje de sombreado de alto nivel (HLSL) como un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="4221f-107">They appear in High Level Shading Language (HLSL) as a constant buffer.</span></span> <span data-ttu-id="4221f-108">Tenga en cuenta que los búferes de constantes para las razones históricas se ven como conjuntos de valores de 4x32 bits.</span><span class="sxs-lookup"><span data-stu-id="4221f-108">Note that constant buffers for historical reasons are viewed as sets of 4x32-bit values.</span></span>

<span data-ttu-id="4221f-109">Cada conjunto de constantes de usuario se trata como una matriz escalar de valores de 32 bits, indexable dinámicamente y de solo lectura desde el sombreador.</span><span class="sxs-lookup"><span data-stu-id="4221f-109">Each set of user constants is treated as a scalar array of 32 -bit values, dynamically indexable and read-only from the shader.</span></span> <span data-ttu-id="4221f-110">Fuera de los límites la indización de un conjunto determinado de constantes raíz produce resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="4221f-110">Out of bounds indexing a given set of root constants produces undefined results.</span></span> <span data-ttu-id="4221f-111">En HLSL, se pueden proporcionar definiciones de estructura de datos para que las constantes de usuario les proporcionen tipos.</span><span class="sxs-lookup"><span data-stu-id="4221f-111">In HLSL, data structure definitions can be provided for the user constants to give them types.</span></span> <span data-ttu-id="4221f-112">Por ejemplo, si la firma raíz define un conjunto de 4 constantes raíz, HLSL puede superponerse a la siguiente estructura en ellas.</span><span class="sxs-lookup"><span data-stu-id="4221f-112">For example, if the root signature defines a set of 4 root constants, HLSL can overlay the following structure on them.</span></span>

``` syntax
struct DrawConstants
{
    uint foo;
    float2 bar;
    int moo;
};
ConstantBuffer<DrawConstants> myDrawConstants : register(b1, space0);
```

<span data-ttu-id="4221f-113">No se permiten matrices en búferes de constantes que se asignan a constantes raíz, ya que no se admite la indexación dinámica en el espacio de la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="4221f-113">Arrays are not permitted in constant buffers that get mapped onto root constants since dynamic indexing in the root signature space is not supported.</span></span> <span data-ttu-id="4221f-114">Por ejemplo, no es válido tener una entrada en el búfer de constantes como `float myArray[2];` .</span><span class="sxs-lookup"><span data-stu-id="4221f-114">For example, it is invalid to have an entry in the constant buffer like `float myArray[2];`.</span></span> <span data-ttu-id="4221f-115">Un búfer de constantes que se asigna a las constantes raíz no puede ser una matriz; por lo tanto, no es válido asignar a `cbuffer myCBArray[2]` constantes raíz.</span><span class="sxs-lookup"><span data-stu-id="4221f-115">A constant buffer that is mapped to root constants cannot itself be an array; therefore, it is invalid to map `cbuffer myCBArray[2]` into root constants.</span></span>

<span data-ttu-id="4221f-116">Las constantes se pueden establecer parcialmente.</span><span class="sxs-lookup"><span data-stu-id="4221f-116">Constants can be partially set.</span></span> <span data-ttu-id="4221f-117">Por ejemplo, si la firma raíz define valores de 4 32 bits en *RootTableBindSlot* 2, cualquier subconjunto de las cuatro constantes se puede establecer a la vez (los demás permanecen sin cambios).</span><span class="sxs-lookup"><span data-stu-id="4221f-117">For example, if the root signature defines four 32-bit values at *RootTableBindSlot* 2, then any subset of the four constants can be set at a time (the others remain unchanged).</span></span> <span data-ttu-id="4221f-118">Esto puede ser útil en agrupaciones que heredan el estado de la firma raíz y pueden cambiarla parcialmente.</span><span class="sxs-lookup"><span data-stu-id="4221f-118">This can be useful in bundles that inherit root signature state and can partially change it.</span></span>

<span data-ttu-id="4221f-119">Al establecer las constantes, preste atención al diseño de búfer de constantes que espera el sombreador.</span><span class="sxs-lookup"><span data-stu-id="4221f-119">When setting constants be careful of the constant buffer layout expected by the shader.</span></span> <span data-ttu-id="4221f-120">Es posible que las constantes se rellenen a `vec4` límites, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4221f-120">It is possible that constants are padded to `vec4` boundaries, for example.</span></span> <span data-ttu-id="4221f-121">Para comprobar el diseño esperado, Compruebe la información de reflexión del sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="4221f-121">To verify the layout expected, check the reflection information from the HLSL shader.</span></span>

<span data-ttu-id="4221f-122">Las siguientes API (de la interfaz [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) ) son para establecer constantes directamente en la firma raíz:</span><span class="sxs-lookup"><span data-stu-id="4221f-122">The following APIs (from the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface) are for setting constants directly on the root signature:</span></span>

-   [<span data-ttu-id="4221f-123">**SetGraphicsRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="4221f-123">**SetGraphicsRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstant)
-   [<span data-ttu-id="4221f-124">**SetGraphicsRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="4221f-124">**SetGraphicsRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsroot32bitconstants)
-   [<span data-ttu-id="4221f-125">**SetComputeRoot32BitConstant**</span><span class="sxs-lookup"><span data-stu-id="4221f-125">**SetComputeRoot32BitConstant**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [<span data-ttu-id="4221f-126">**SetComputeRoot32BitConstants**</span><span class="sxs-lookup"><span data-stu-id="4221f-126">**SetComputeRoot32BitConstants**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)

<span data-ttu-id="4221f-127">Además, consulte la estructura [**de \_ \_ constantes**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) de la raíz de D3D12.</span><span class="sxs-lookup"><span data-stu-id="4221f-127">Also, refer to the [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4221f-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4221f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4221f-129">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="4221f-129">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




