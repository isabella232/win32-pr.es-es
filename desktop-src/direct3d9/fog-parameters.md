---
description: Los parámetros de niebla se controlan a través de los Estados de representación del dispositivo.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Parámetros de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906544"
---
# <a name="fog-parameters-direct3d-9"></a><span data-ttu-id="717c0-103">Parámetros de niebla (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="717c0-103">Fog Parameters (Direct3D 9)</span></span>

<span data-ttu-id="717c0-104">Los parámetros de niebla se controlan a través de los Estados de representación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="717c0-104">Fog parameters are controlled through device render states.</span></span> <span data-ttu-id="717c0-105">Los tipos de niebla de píxeles y vértices admiten todas las fórmulas de niebla introducidas en [fórmulas de niebla (Direct3D 9)](fog-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="717c0-105">Both pixel and vertex fog types support all the fog formulas introduced in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="717c0-106">El tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) define constantes que se pueden usar para identificar la fórmula de niebla que se desea que utilice Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="717c0-106">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type defines constants that you can use to identify the fog formula you want Microsoft Direct3D to use.</span></span> <span data-ttu-id="717c0-107">El estado de representación de D3DRS \_ FOGTABLEMODE controla el modo de niebla que Direct3D usa para la niebla de píxeles y el \_ Estado de representación de D3DRS FOGVERTEXMODE controla el modo de niebla de vértices.</span><span class="sxs-lookup"><span data-stu-id="717c0-107">The D3DRS\_FOGTABLEMODE render state controls the fog mode that Direct3D uses for pixel fog, and the D3DRS\_FOGVERTEXMODE render state controls the mode for vertex fog.</span></span>

<span data-ttu-id="717c0-108">Al usar la fórmula de niebla lineal, establezca las distancias inicial y final mediante los \_ Estados de representación D3DRS FOGSTART y D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="717c0-108">When using the linear fog formula, you set the starting and ending distances through the D3DRS\_FOGSTART and D3DRS\_FOGEND render states.</span></span> <span data-ttu-id="717c0-109">La forma en que el sistema interprete estos valores depende del tipo de niebla que use la aplicación: la niebla de píxeles o de vértices y, cuando se usa la niebla de píxeles, si se usa la profundidad basada en z o en w.</span><span class="sxs-lookup"><span data-stu-id="717c0-109">How the system interprets these values depends on the type of fog your application uses - pixel or vertex fog - and, when using pixel fog, if z-based or w-based depth is being used.</span></span> <span data-ttu-id="717c0-110">En la tabla siguiente se resumen los tipos de niebla y sus unidades de inicio y finalización.</span><span class="sxs-lookup"><span data-stu-id="717c0-110">The following table summarizes fog types and their start and end units.</span></span>



| <span data-ttu-id="717c0-111">Tipo de niebla</span><span class="sxs-lookup"><span data-stu-id="717c0-111">Fog type</span></span>  | <span data-ttu-id="717c0-112">Unidades de inicio y finalización de niebla</span><span class="sxs-lookup"><span data-stu-id="717c0-112">Fog start/end units</span></span>      |
|-----------|--------------------------|
| <span data-ttu-id="717c0-113">Píxel (Z)</span><span class="sxs-lookup"><span data-stu-id="717c0-113">Pixel (Z)</span></span> | <span data-ttu-id="717c0-114">Espacio \[ de dispositivo 0.0, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="717c0-114">Device space \[0.0,1.0\]</span></span> |
| <span data-ttu-id="717c0-115">Píxel (W)</span><span class="sxs-lookup"><span data-stu-id="717c0-115">Pixel (W)</span></span> | <span data-ttu-id="717c0-116">Espacio de la cámara</span><span class="sxs-lookup"><span data-stu-id="717c0-116">Camera space</span></span>             |
| <span data-ttu-id="717c0-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="717c0-117">Vertex</span></span>    | <span data-ttu-id="717c0-118">Espacio de la cámara</span><span class="sxs-lookup"><span data-stu-id="717c0-118">Camera space</span></span>             |



 

<span data-ttu-id="717c0-119">El estado de representación de D3DRS \_ FOGDENSITY controla la densidad de niebla aplicada cuando se habilita una fórmula de niebla exponencial.</span><span class="sxs-lookup"><span data-stu-id="717c0-119">The D3DRS\_FOGDENSITY render state controls the fog density applied when an exponential fog formula is enabled.</span></span> <span data-ttu-id="717c0-120">La densidad de niebla es esencialmente un factor de ponderación, comprendido entre 0,0 y 1,0 (incluido), que escala el valor de distancia en el exponente.</span><span class="sxs-lookup"><span data-stu-id="717c0-120">Fog density is essentially a weighting factor, ranging from 0.0 to 1.0 (inclusive), that scales the distance value in the exponent.</span></span>

<span data-ttu-id="717c0-121">El color que utiliza el sistema para la combinación de niebla se controla a través del \_ Estado de representación del dispositivo D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="717c0-121">The color that the system uses for fog blending is controlled through the D3DRS\_FOGCOLOR device render state.</span></span> <span data-ttu-id="717c0-122">Para obtener más información, vea el [color de niebla (Direct3D 9)](fog-color.md) y la [combinación de niebla (Direct3D 9)](fog-blending.md).</span><span class="sxs-lookup"><span data-stu-id="717c0-122">For more information, see [Fog Color (Direct3D 9)](fog-color.md) and [Fog Blending (Direct3D 9)](fog-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="717c0-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="717c0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="717c0-124">Tipos de niebla</span><span class="sxs-lookup"><span data-stu-id="717c0-124">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
