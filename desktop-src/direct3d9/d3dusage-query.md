---
description: Estas opciones identifican los tipos de recursos de consulta.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038cb64b1ad4f5f7ee2dd78ffc2e2a5ebab90d0e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342990"
---
# <a name="d3dusage_query"></a><span data-ttu-id="6bf62-103">CONSULTA D3DUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="6bf62-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="6bf62-104">Estas opciones identifican los tipos de recursos de consulta.</span><span class="sxs-lookup"><span data-stu-id="6bf62-104">These options identify query resource types.</span></span>



| <span data-ttu-id="6bf62-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="6bf62-105">\#define</span></span>                                   | <span data-ttu-id="6bf62-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6bf62-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf62-107">FILTRO DE CONSULTA D3DUSAGE \_ \_</span><span class="sxs-lookup"><span data-stu-id="6bf62-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="6bf62-108">Consulte el formato de recurso para ver si admite tipos de filtro de textura distintos de D3DTEXF \_ POINT (que siempre se admite).</span><span class="sxs-lookup"><span data-stu-id="6bf62-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="6bf62-109">D3DUSAGE \_ QUERY \_ LEGACYBUMPMAP</span><span class="sxs-lookup"><span data-stu-id="6bf62-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="6bf62-110">Consulte el recurso sobre un mapa de rendimiento heredado.</span><span class="sxs-lookup"><span data-stu-id="6bf62-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6bf62-111">COMBINACIÓN DE \_ POSTPIXELSHADER DE CONSULTA D3DUSAGE \_ \_</span><span class="sxs-lookup"><span data-stu-id="6bf62-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="6bf62-112">Consulte el recurso para comprobar la compatibilidad con la combinación posterior del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="6bf62-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="6bf62-113">Si Se produce un error en [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ QUERY \_ POSTPIXELSHADER BLENDING, no se admiten las operaciones de combinación de píxeles \_ posteriores.</span><span class="sxs-lookup"><span data-stu-id="6bf62-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="6bf62-114">Entre ellas se incluyen la prueba alfa, píxeles de píxeles, mezcla de destino de representación, habilitación de escritura de color y dithering.</span><span class="sxs-lookup"><span data-stu-id="6bf62-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="6bf62-115">D3DUSAGE \_ QUERY \_ SRGBREAD</span><span class="sxs-lookup"><span data-stu-id="6bf62-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="6bf62-116">Consulte el recurso para comprobar si una textura admite la corrección gamma durante una operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="6bf62-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6bf62-117">D3DUSAGE \_ QUERY \_ SRGBWRITE</span><span class="sxs-lookup"><span data-stu-id="6bf62-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="6bf62-118">Consulte el recurso para comprobar si una textura admite la corrección gamma durante una operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="6bf62-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="6bf62-119">VÉRTICE DE CONSULTA D3DUSAGETEXTURE \_ \_</span><span class="sxs-lookup"><span data-stu-id="6bf62-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="6bf62-120">Consulte el recurso para comprobar la compatibilidad con el muestreo de textura del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="6bf62-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="6bf62-121">D3DUSAGE \_ QUERY \_ WRAPANDMIP</span><span class="sxs-lookup"><span data-stu-id="6bf62-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="6bf62-122">Consulte el recurso para comprobar la compatibilidad con el ajuste de texturas y la asignación de mip.</span><span class="sxs-lookup"><span data-stu-id="6bf62-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="6bf62-123">Use [**CheckDeviceFormat para**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) consultar la compatibilidad de hardware para estos usos y otros usos enumerados en [D3DUSAGE](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="6bf62-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="6bf62-124">Información constante</span><span class="sxs-lookup"><span data-stu-id="6bf62-124">Constant Information</span></span>



| <span data-ttu-id="6bf62-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bf62-125">Requirement</span></span>                         | <span data-ttu-id="6bf62-126">Value</span><span class="sxs-lookup"><span data-stu-id="6bf62-126">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="6bf62-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bf62-127">Header</span></span>                   | <span data-ttu-id="6bf62-128">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="6bf62-128">d3d9types.h</span></span> |
| <span data-ttu-id="6bf62-129">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="6bf62-129">Minimum operating system</span></span> | <span data-ttu-id="6bf62-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6bf62-130">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="6bf62-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6bf62-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bf62-132">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="6bf62-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
