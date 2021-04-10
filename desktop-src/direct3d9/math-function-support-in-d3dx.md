---
description: D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152321"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="2fcc6-104">Compatibilidad con funciones matemáticas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2fcc6-104">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="2fcc6-105">D3DX es una biblioteca de utilidades que proporciona servicios auxiliares.</span><span class="sxs-lookup"><span data-stu-id="2fcc6-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="2fcc6-106">Es una capa por encima del componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2fcc6-106">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="2fcc6-107">Matemáticas</span><span class="sxs-lookup"><span data-stu-id="2fcc6-107">Math</span></span>

<span data-ttu-id="2fcc6-108">La compatibilidad con matemáticas, contenida en un conjunto de funciones, se proporciona para:</span><span class="sxs-lookup"><span data-stu-id="2fcc6-108">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="2fcc6-109">Cálculos de color</span><span class="sxs-lookup"><span data-stu-id="2fcc6-109">Color calculations</span></span>
-   <span data-ttu-id="2fcc6-110">Planos</span><span class="sxs-lookup"><span data-stu-id="2fcc6-110">Planes</span></span>
-   <span data-ttu-id="2fcc6-111">Manipulación de la matriz</span><span class="sxs-lookup"><span data-stu-id="2fcc6-111">Matrix manipulation</span></span>
-   <span data-ttu-id="2fcc6-112">Cuaterniones</span><span class="sxs-lookup"><span data-stu-id="2fcc6-112">Quaternions</span></span>
-   <span data-ttu-id="2fcc6-113">vectores 2D</span><span class="sxs-lookup"><span data-stu-id="2fcc6-113">2D vectors</span></span>
-   <span data-ttu-id="2fcc6-114">vectores 3D</span><span class="sxs-lookup"><span data-stu-id="2fcc6-114">3D vectors</span></span>
-   <span data-ttu-id="2fcc6-115">4D (vectores)</span><span class="sxs-lookup"><span data-stu-id="2fcc6-115">4D vectors</span></span>

<span data-ttu-id="2fcc6-116">Tenga en cuenta que, cuando se combina con las sobrecargas de C++, la compatibilidad con los tipos básicos de matemáticas 3D es extensa.</span><span class="sxs-lookup"><span data-stu-id="2fcc6-116">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="2fcc6-117">Para obtener más información sobre estas funciones, consulte [funciones de D3DX](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="2fcc6-117">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="2fcc6-118">Para ayudar a encontrar la función que necesita, se dividen en varias carpetas.</span><span class="sxs-lookup"><span data-stu-id="2fcc6-118">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="2fcc6-119">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="2fcc6-119">FLOAT16</span></span>

<span data-ttu-id="2fcc6-120">Al usar el tipo de datos FLOAT16, asegúrese de limitar los valores a un máximo de D3DX \_ 16F \_ Max.</span><span class="sxs-lookup"><span data-stu-id="2fcc6-120">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="2fcc6-121">Cualquier valor de FLOAT16 que supere esto dará lugar a un comportamiento indefinido en la canalización.</span><span class="sxs-lookup"><span data-stu-id="2fcc6-121">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="2fcc6-122">Vea [otras constantes de D3DX](other-d3dx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2fcc6-122">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fcc6-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2fcc6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fcc6-124">D3DX</span><span class="sxs-lookup"><span data-stu-id="2fcc6-124">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



