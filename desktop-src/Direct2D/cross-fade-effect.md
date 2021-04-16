---
title: Efecto de atenuación cruzada
description: Este efecto combina dos imágenes mediante la adición de píxeles ponderados de las imágenes de entrada. Tiene dos entradas, denominadas destino y origen.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534114"
---
# <a name="cross-fade-effect"></a><span data-ttu-id="7bda4-104">Efecto de atenuación cruzada</span><span class="sxs-lookup"><span data-stu-id="7bda4-104">Cross-fade effect</span></span>

<span data-ttu-id="7bda4-105">Este efecto combina dos imágenes mediante la adición de píxeles ponderados de las imágenes de entrada.</span><span class="sxs-lookup"><span data-stu-id="7bda4-105">This effect combines two images by adding weighted pixels from input images.</span></span> <span data-ttu-id="7bda4-106">Tiene dos entradas, denominadas destino y origen.</span><span class="sxs-lookup"><span data-stu-id="7bda4-106">It has two inputs, named Destination and Source.</span></span>

<span data-ttu-id="7bda4-107">La fórmula de atenuación cruzada es **salida = destino de peso \* + (1-peso) \* origen**.</span><span class="sxs-lookup"><span data-stu-id="7bda4-107">The cross fade formula is **output = weight \* Destination + (1 - weight) \* Source**.</span></span>

<span data-ttu-id="7bda4-108">El CLSID para este efecto es CLSID \_ D2D1CrossFade.</span><span class="sxs-lookup"><span data-stu-id="7bda4-108">The CLSID for this effect is CLSID\_D2D1CrossFade.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="7bda4-109">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="7bda4-109">Effect properties</span></span>

| <span data-ttu-id="7bda4-110">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="7bda4-110">Display name and index enumeration</span></span>             | <span data-ttu-id="7bda4-111">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7bda4-111">Type and default value</span></span> | <span data-ttu-id="7bda4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bda4-112">Description</span></span>                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bda4-113">Peso de la WeightD2D1 con \_ fundido cruzado \_ \_</span><span class="sxs-lookup"><span data-stu-id="7bda4-113">WeightD2D1\_CROSSFADE\_PROP\_WEIGHT</span></span><br/> | <span data-ttu-id="7bda4-114">FLOAT 0.5 f</span><span class="sxs-lookup"><span data-stu-id="7bda4-114">FLOAT0.5f</span></span><br/>   | <span data-ttu-id="7bda4-115">Cuántos pesan los valores de color de la imagen de origen frente a la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="7bda4-115">How much to weigh the source image color values versus the destination image.</span></span> <span data-ttu-id="7bda4-116">El valor mínimo es 0.0 f (usar exclusivamente la imagen de destino para determinar el resultado) y el valor máximo es 1.0 f (usar exclusivamente la imagen de origen para determinar la salida).</span><span class="sxs-lookup"><span data-stu-id="7bda4-116">The minimum value is 0.0f (exclusively use the destination image to determine the output) and the maximum value is 1.0f (exclusively use the source image to determine the output).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7bda4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bda4-117">Requirements</span></span>



| <span data-ttu-id="7bda4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bda4-118">Requirement</span></span> | <span data-ttu-id="7bda4-119">Value</span><span class="sxs-lookup"><span data-stu-id="7bda4-119">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="7bda4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bda4-120">Minimum supported client</span></span> | <span data-ttu-id="7bda4-121">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="7bda4-121">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7bda4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bda4-122">Minimum supported server</span></span> | <span data-ttu-id="7bda4-123">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="7bda4-123">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7bda4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bda4-124">Header</span></span>                   | <span data-ttu-id="7bda4-125">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="7bda4-125">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="7bda4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7bda4-126">Library</span></span>                  | <span data-ttu-id="7bda4-127">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7bda4-127">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="7bda4-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bda4-128">Related topics</span></span>

* [<span data-ttu-id="7bda4-129">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="7bda4-129">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
