---
description: Estas opciones identifican los tipos de recursos de consulta.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f5dda7f84dfa36e4f3b7ece1b359a4841bbbf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153126"
---
# <a name="d3dusage_query"></a><span data-ttu-id="7ca5d-103">\_Consulta D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="7ca5d-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="7ca5d-104">Estas opciones identifican los tipos de recursos de consulta.</span><span class="sxs-lookup"><span data-stu-id="7ca5d-104">These options identify query resource types.</span></span>



|                                            |                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca5d-105">\#define</span><span class="sxs-lookup"><span data-stu-id="7ca5d-105">\#define</span></span>                                   | <span data-ttu-id="7ca5d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ca5d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7ca5d-107">\_Filtro de consulta D3DUSAGE \_</span><span class="sxs-lookup"><span data-stu-id="7ca5d-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="7ca5d-108">Consulte el formato de recursos para ver si admite tipos de filtro de textura distintos \_ del punto D3DTEXF (que siempre se admite).</span><span class="sxs-lookup"><span data-stu-id="7ca5d-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="7ca5d-109">\_LEGACYBUMPMAP consulta \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="7ca5d-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="7ca5d-110">Consultar el recurso sobre un mapa de rugosidad heredado.</span><span class="sxs-lookup"><span data-stu-id="7ca5d-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7ca5d-111">D3DUSAGE \_ consulta \_ POSTPIXELSHADER \_ blending</span><span class="sxs-lookup"><span data-stu-id="7ca5d-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="7ca5d-112">Consulte el recurso para comprobar la compatibilidad con la compatibilidad con la fusión de sombreador de píxeles post.</span><span class="sxs-lookup"><span data-stu-id="7ca5d-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="7ca5d-113">Si [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) produce un error con D3DUSAGE \_ query \_ POSTPIXELSHADER \_ blending, no se admiten las operaciones de combinación de píxeles post.</span><span class="sxs-lookup"><span data-stu-id="7ca5d-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="7ca5d-114">Entre ellas se incluyen la prueba alfa, la niebla de píxeles, la mezcla de destino de representación, la habilitación de escritura de color y la interpolación.</span><span class="sxs-lookup"><span data-stu-id="7ca5d-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="7ca5d-115">\_SRGBREAD consulta \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="7ca5d-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="7ca5d-116">Consulte el recurso para comprobar si una textura admite la corrección gamma durante una operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="7ca5d-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7ca5d-117">\_SRGBWRITE consulta \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="7ca5d-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="7ca5d-118">Consulte el recurso para comprobar si una textura admite la corrección gamma durante una operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="7ca5d-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="7ca5d-119">\_VERTEXTEXTURE consulta \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="7ca5d-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="7ca5d-120">Consulte el recurso para comprobar la compatibilidad con el muestreo de textura del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="7ca5d-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7ca5d-121">\_WRAPANDMIP consulta \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="7ca5d-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="7ca5d-122">Consulte el recurso para comprobar la compatibilidad con el ajuste de textura y la asignación de MIP.</span><span class="sxs-lookup"><span data-stu-id="7ca5d-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="7ca5d-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) para consultar la compatibilidad de hardware para estos usos y otros usos que se enumeran en [D3DUSAGE](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="7ca5d-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="7ca5d-124">Información constante</span><span class="sxs-lookup"><span data-stu-id="7ca5d-124">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="7ca5d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ca5d-125">Header</span></span>                   | <span data-ttu-id="7ca5d-126">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="7ca5d-126">d3d9types.h</span></span> |
| <span data-ttu-id="7ca5d-127">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="7ca5d-127">Minimum operating system</span></span> | <span data-ttu-id="7ca5d-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7ca5d-128">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="7ca5d-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ca5d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ca5d-130">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7ca5d-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
