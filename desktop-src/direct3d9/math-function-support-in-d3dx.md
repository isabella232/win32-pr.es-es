---
description: Obtenga información sobre la compatibilidad con funciones matemáticas en D3DX. D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28c32b13d185694e4ffa41c314cf9f77cbb18b7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407528"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="0f831-105">Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0f831-105">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="0f831-106">D3DX es una biblioteca de utilidades que proporciona servicios auxiliares.</span><span class="sxs-lookup"><span data-stu-id="0f831-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="0f831-107">Es una capa por encima del componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="0f831-107">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="0f831-108">Matemáticas</span><span class="sxs-lookup"><span data-stu-id="0f831-108">Math</span></span>

<span data-ttu-id="0f831-109">La compatibilidad matemática, contenida en un conjunto de funciones, se proporciona para:</span><span class="sxs-lookup"><span data-stu-id="0f831-109">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="0f831-110">Cálculos de color</span><span class="sxs-lookup"><span data-stu-id="0f831-110">Color calculations</span></span>
-   <span data-ttu-id="0f831-111">Aviones</span><span class="sxs-lookup"><span data-stu-id="0f831-111">Planes</span></span>
-   <span data-ttu-id="0f831-112">Manipulación de matriz</span><span class="sxs-lookup"><span data-stu-id="0f831-112">Matrix manipulation</span></span>
-   <span data-ttu-id="0f831-113">Cuaterniones</span><span class="sxs-lookup"><span data-stu-id="0f831-113">Quaternions</span></span>
-   <span data-ttu-id="0f831-114">Vectores 2D</span><span class="sxs-lookup"><span data-stu-id="0f831-114">2D vectors</span></span>
-   <span data-ttu-id="0f831-115">Vectores 3D</span><span class="sxs-lookup"><span data-stu-id="0f831-115">3D vectors</span></span>
-   <span data-ttu-id="0f831-116">Vectores 4D</span><span class="sxs-lookup"><span data-stu-id="0f831-116">4D vectors</span></span>

<span data-ttu-id="0f831-117">Tenga en cuenta que, cuando se combina con las sobrecargas de C++, la compatibilidad con los tipos matemáticos 3D básicos es amplia.</span><span class="sxs-lookup"><span data-stu-id="0f831-117">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="0f831-118">Para obtener más información sobre estas funciones, vea [Funciones D3DX](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0f831-118">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="0f831-119">Para ayudar a encontrar la función que necesita, se divide en varias carpetas.</span><span class="sxs-lookup"><span data-stu-id="0f831-119">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="0f831-120">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0f831-120">FLOAT16</span></span>

<span data-ttu-id="0f831-121">Al usar el tipo de datos FLOAT16, asegúrese de limitar los valores a un máximo de D3DX \_ 16F \_ MAX.</span><span class="sxs-lookup"><span data-stu-id="0f831-121">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="0f831-122">Cualquier valor FLOAT16 que supere esto dará lugar a un comportamiento indefinido en la canalización.</span><span class="sxs-lookup"><span data-stu-id="0f831-122">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="0f831-123">Vea [Otras constantes D3DX](other-d3dx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0f831-123">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f831-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0f831-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f831-125">D3DX</span><span class="sxs-lookup"><span data-stu-id="0f831-125">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



