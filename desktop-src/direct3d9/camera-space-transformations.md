---
description: Los vértices del espacio de la cámara se calculan transformando los vértices del objeto con la matriz de la vista mundial.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Transformaciones del espacio de la cámara (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153129"
---
# <a name="camera-space-transformations-direct3d-9"></a><span data-ttu-id="0e863-103">Transformaciones del espacio de la cámara (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0e863-103">Camera Space Transformations (Direct3D 9)</span></span>

<span data-ttu-id="0e863-104">Los vértices del espacio de la cámara se calculan transformando los vértices del objeto con la matriz de la vista mundial.</span><span class="sxs-lookup"><span data-stu-id="0e863-104">Vertices in the camera space are computed by transforming the object vertices with the world view matrix.</span></span>

<span data-ttu-id="0e863-105">V = V \* wvMatrix</span><span class="sxs-lookup"><span data-stu-id="0e863-105">V = V \* wvMatrix</span></span>

<span data-ttu-id="0e863-106">Las normales de vértice, en el espacio de la cámara, se calculan transformando las normales del objeto con la transformación inversa de la matriz de la vista mundial.</span><span class="sxs-lookup"><span data-stu-id="0e863-106">Vertex normals, in camera space, are computed by transforming the object normals with the inverse transpose of the world view matrix.</span></span> <span data-ttu-id="0e863-107">La matriz de vista mundial puede o no ser ortogonal.</span><span class="sxs-lookup"><span data-stu-id="0e863-107">The world view matrix may or may not be orthogonal.</span></span>

<span data-ttu-id="0e863-108">N = N \* (wvMatrix ⁻ ¹)<sup>T</sup></span><span class="sxs-lookup"><span data-stu-id="0e863-108">N = N \* (wvMatrix⁻¹)<sup>T</sup></span></span>

<span data-ttu-id="0e863-109">La inversión de matriz y la conversión de matriz operan en una matriz de 4x4.</span><span class="sxs-lookup"><span data-stu-id="0e863-109">The matrix inversion and matrix transpose operate on a 4x4 matrix.</span></span> <span data-ttu-id="0e863-110">La multiplicación combina el normal con la parte 3x3 de la matriz 4x4 resultante.</span><span class="sxs-lookup"><span data-stu-id="0e863-110">The multiply combines the normal with the 3x3 portion of the resulting 4x4 matrix.</span></span>

<span data-ttu-id="0e863-111">Si el estado de representación, D3DRENDERSTATE \_ NORMALIZENORMALS se establece en **true**, los vectores normales de vértices se normalizan después de la transformación en el espacio de la cámara como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="0e863-111">If the render state, D3DRENDERSTATE\_NORMALIZENORMALS is set to **TRUE**, vertex normal vectors are normalized after transformation to camera space as follows:</span></span>

<span data-ttu-id="0e863-112">N = norma (N)</span><span class="sxs-lookup"><span data-stu-id="0e863-112">N = norm(N)</span></span>

<span data-ttu-id="0e863-113">La posición de la luz en el espacio de la cámara se calcula transformando la posición de la fuente de luz con la matriz de la vista.</span><span class="sxs-lookup"><span data-stu-id="0e863-113">Light position in camera space is computed by transforming the light source position with the view matrix.</span></span>

<span data-ttu-id="0e863-114">LP = LP \* vMatrix</span><span class="sxs-lookup"><span data-stu-id="0e863-114">Lₚ = Lₚ \* vMatrix</span></span>

<span data-ttu-id="0e863-115">La dirección de la luz en el espacio de la cámara para una luz direccional se calcula multiplicando la dirección de origen de la luz por la matriz de la vista, normalizando y negando el resultado.</span><span class="sxs-lookup"><span data-stu-id="0e863-115">The direction to the light in camera space for a directional light is computed by multiplying the light source direction by the view matrix, normalizing, and negating the result.</span></span>

<span data-ttu-id="0e863-116">L<sub>dir</sub> =-norma (L<sub>dir</sub> \* wvMatrix)</span><span class="sxs-lookup"><span data-stu-id="0e863-116">L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)</span></span>

<span data-ttu-id="0e863-117">En el caso del \_ punto D3DLIGHT y D3DLIGHT, \_ la dirección de la luz se calcula de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="0e863-117">For the D3DLIGHT\_POINT and D3DLIGHT\_SPOT the direction to light is computed as follows:</span></span>

<span data-ttu-id="0e863-118">L<sub>dir</sub> = norma (V \* LP), donde los parámetros se definen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0e863-118">L<sub>dir</sub> = norm(V \* Lₚ), where the parameters are defined in the following table.</span></span>



| <span data-ttu-id="0e863-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0e863-119">Parameter</span></span>       | <span data-ttu-id="0e863-120">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0e863-120">Default value</span></span> | <span data-ttu-id="0e863-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e863-121">Type</span></span>      | <span data-ttu-id="0e863-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e863-122">Description</span></span>                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <span data-ttu-id="0e863-123"><sub>Directorio</sub> L</span><span class="sxs-lookup"><span data-stu-id="0e863-123">L<sub>dir</sub></span></span> | <span data-ttu-id="0e863-124">N/D</span><span class="sxs-lookup"><span data-stu-id="0e863-124">N/A</span></span>           | <span data-ttu-id="0e863-125">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0e863-125">D3DVECTOR</span></span> | <span data-ttu-id="0e863-126">Vector de dirección desde el vértice del objeto hasta la luz</span><span class="sxs-lookup"><span data-stu-id="0e863-126">Direction vector from object vertex to the light</span></span>          |
| <span data-ttu-id="0e863-127">V</span><span class="sxs-lookup"><span data-stu-id="0e863-127">V</span></span>               | <span data-ttu-id="0e863-128">N/D</span><span class="sxs-lookup"><span data-stu-id="0e863-128">N/A</span></span>           | <span data-ttu-id="0e863-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0e863-129">D3DVECTOR</span></span> | <span data-ttu-id="0e863-130">Posición del vértice en el espacio de la cámara</span><span class="sxs-lookup"><span data-stu-id="0e863-130">Vertex position in camera space</span></span>                           |
| <span data-ttu-id="0e863-131">wvMatrix</span><span class="sxs-lookup"><span data-stu-id="0e863-131">wvMatrix</span></span>        | <span data-ttu-id="0e863-132">Identidad</span><span class="sxs-lookup"><span data-stu-id="0e863-132">Identity</span></span>      | <span data-ttu-id="0e863-133">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="0e863-133">D3DMATRIX</span></span> | <span data-ttu-id="0e863-134">Matriz compuesta que contiene las transformaciones mundo y vista</span><span class="sxs-lookup"><span data-stu-id="0e863-134">Composite matrix containing the world and view transforms</span></span> |
| <span data-ttu-id="0e863-135">N</span><span class="sxs-lookup"><span data-stu-id="0e863-135">N</span></span>               | <span data-ttu-id="0e863-136">N/D</span><span class="sxs-lookup"><span data-stu-id="0e863-136">N/A</span></span>           | <span data-ttu-id="0e863-137">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0e863-137">D3DVECTOR</span></span> | <span data-ttu-id="0e863-138">Vértice normal</span><span class="sxs-lookup"><span data-stu-id="0e863-138">Vertex normal</span></span>                                             |
| <span data-ttu-id="0e863-139">LP</span><span class="sxs-lookup"><span data-stu-id="0e863-139">Lₚ</span></span>              | <span data-ttu-id="0e863-140">N/D</span><span class="sxs-lookup"><span data-stu-id="0e863-140">N/A</span></span>           | <span data-ttu-id="0e863-141">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0e863-141">D3DVECTOR</span></span> | <span data-ttu-id="0e863-142">Posición clara en el espacio de la cámara</span><span class="sxs-lookup"><span data-stu-id="0e863-142">Light position in camera space</span></span>                            |
| <span data-ttu-id="0e863-143">vMatrix</span><span class="sxs-lookup"><span data-stu-id="0e863-143">vMatrix</span></span>         | <span data-ttu-id="0e863-144">Identidad</span><span class="sxs-lookup"><span data-stu-id="0e863-144">Identity</span></span>      | <span data-ttu-id="0e863-145">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="0e863-145">D3DMATRIX</span></span> | <span data-ttu-id="0e863-146">Matriz que contiene la transformación de la vista</span><span class="sxs-lookup"><span data-stu-id="0e863-146">Matrix containing the view transform</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="0e863-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e863-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e863-148">Matemáticas de iluminación</span><span class="sxs-lookup"><span data-stu-id="0e863-148">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



