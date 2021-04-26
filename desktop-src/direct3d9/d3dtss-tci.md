---
description: Marcas de funcionalidad de coordenada de textura del controlador.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da9ca23ebc4dd121527721a9d10a2db55a4d555
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995262"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="67fdb-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="67fdb-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="67fdb-104">Marcas de funcionalidad de coordenada de textura del controlador.</span><span class="sxs-lookup"><span data-stu-id="67fdb-104">Driver texture coordinate capability flags.</span></span>



| <span data-ttu-id="67fdb-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="67fdb-105">\#define</span></span>                                 | <span data-ttu-id="67fdb-106">Value</span><span class="sxs-lookup"><span data-stu-id="67fdb-106">Value</span></span>       | <span data-ttu-id="67fdb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="67fdb-107">Description</span></span>                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67fdb-108">D3DTSS \_ TCI \_ PASSTHRU</span><span class="sxs-lookup"><span data-stu-id="67fdb-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="67fdb-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="67fdb-109">0x00000000L</span></span> | <span data-ttu-id="67fdb-110">Use las coordenadas de textura especificadas contenidas en el formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="67fdb-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="67fdb-111">Este valor se resuelve en cero.</span><span class="sxs-lookup"><span data-stu-id="67fdb-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="67fdb-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="67fdb-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="67fdb-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="67fdb-113">0x00010000L</span></span> | <span data-ttu-id="67fdb-114">Use el vértice normal, transformado en espacio de la cámara, como coordenadas de textura de entrada para la transformación de textura de esta fase.</span><span class="sxs-lookup"><span data-stu-id="67fdb-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="67fdb-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="67fdb-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="67fdb-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="67fdb-116">0x00020000L</span></span> | <span data-ttu-id="67fdb-117">Use la posición del vértice, transformada en espacio de la cámara, como coordenadas de textura de entrada para la transformación de textura de esta fase.</span><span class="sxs-lookup"><span data-stu-id="67fdb-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="67fdb-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="67fdb-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="67fdb-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="67fdb-119">0x00030000L</span></span> | <span data-ttu-id="67fdb-120">Use el vector de reflexión, transformado en espacio de la cámara, como coordenada de textura de entrada para la transformación de textura de esta fase.</span><span class="sxs-lookup"><span data-stu-id="67fdb-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="67fdb-121">El vector de reflexión se calcula a partir de la posición del vértice de entrada y el vector normal.</span><span class="sxs-lookup"><span data-stu-id="67fdb-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="67fdb-122">MAPA DE ESFERA \_ DE TCI de D3DTSS \_</span><span class="sxs-lookup"><span data-stu-id="67fdb-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="67fdb-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="67fdb-123">0x00040000L</span></span> | <span data-ttu-id="67fdb-124">Use las coordenadas de textura especificadas para la asignación de esferas.</span><span class="sxs-lookup"><span data-stu-id="67fdb-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="67fdb-125">D3DTSS \_ TEXCOORDINDEX usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="67fdb-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="67fdb-126">Información constante</span><span class="sxs-lookup"><span data-stu-id="67fdb-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="67fdb-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67fdb-127">Header</span></span>                   | <span data-ttu-id="67fdb-128">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="67fdb-128">d3d9caps.h</span></span> |
| <span data-ttu-id="67fdb-129">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="67fdb-129">Minimum operating system</span></span> | <span data-ttu-id="67fdb-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="67fdb-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="67fdb-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67fdb-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67fdb-132">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="67fdb-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



