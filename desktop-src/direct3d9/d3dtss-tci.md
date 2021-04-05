---
description: Marcas de capacidad de coordenadas de textura del controlador.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000777"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="4dee0-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="4dee0-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="4dee0-104">Marcas de capacidad de coordenadas de textura del controlador.</span><span class="sxs-lookup"><span data-stu-id="4dee0-104">Driver texture coordinate capability flags.</span></span>



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dee0-105">\#define</span><span class="sxs-lookup"><span data-stu-id="4dee0-105">\#define</span></span>                                 | <span data-ttu-id="4dee0-106">Value</span><span class="sxs-lookup"><span data-stu-id="4dee0-106">Value</span></span>       | <span data-ttu-id="4dee0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dee0-107">Description</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="4dee0-108">D3DTSS \_ TCI \_ PASSTHRU</span><span class="sxs-lookup"><span data-stu-id="4dee0-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="4dee0-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="4dee0-109">0x00000000L</span></span> | <span data-ttu-id="4dee0-110">Usar las coordenadas de textura especificadas contenidas en el formato de vértices.</span><span class="sxs-lookup"><span data-stu-id="4dee0-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="4dee0-111">Este valor se resuelve como cero.</span><span class="sxs-lookup"><span data-stu-id="4dee0-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="4dee0-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="4dee0-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="4dee0-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="4dee0-113">0x00010000L</span></span> | <span data-ttu-id="4dee0-114">Use el vértice normal, transformado en el espacio de la cámara, como coordenadas de textura de entrada para la transformación de textura de esta fase.</span><span class="sxs-lookup"><span data-stu-id="4dee0-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="4dee0-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="4dee0-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="4dee0-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="4dee0-116">0x00020000L</span></span> | <span data-ttu-id="4dee0-117">Use la posición del vértice, transformada en el espacio de la cámara, como coordenadas de textura de entrada para la transformación de textura de esta fase.</span><span class="sxs-lookup"><span data-stu-id="4dee0-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="4dee0-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="4dee0-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="4dee0-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="4dee0-119">0x00030000L</span></span> | <span data-ttu-id="4dee0-120">Use el vector de reflexión, transformado en el espacio de la cámara, como la coordenada de textura de entrada para la transformación de textura de esta fase.</span><span class="sxs-lookup"><span data-stu-id="4dee0-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="4dee0-121">El vector de reflexión se calcula a partir de la posición del vértice de entrada y del vector normal.</span><span class="sxs-lookup"><span data-stu-id="4dee0-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="4dee0-122">D3DTSS \_ TCI \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="4dee0-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="4dee0-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="4dee0-123">0x00040000L</span></span> | <span data-ttu-id="4dee0-124">Usar las coordenadas de textura especificadas para la asignación de esferas.</span><span class="sxs-lookup"><span data-stu-id="4dee0-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="4dee0-125">D3DTSS TEXCOORDINDEX usa estas constantes \_ .</span><span class="sxs-lookup"><span data-stu-id="4dee0-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="4dee0-126">Información constante</span><span class="sxs-lookup"><span data-stu-id="4dee0-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="4dee0-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4dee0-127">Header</span></span>                   | <span data-ttu-id="4dee0-128">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="4dee0-128">d3d9caps.h</span></span> |
| <span data-ttu-id="4dee0-129">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="4dee0-129">Minimum operating system</span></span> | <span data-ttu-id="4dee0-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="4dee0-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4dee0-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4dee0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dee0-132">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="4dee0-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



