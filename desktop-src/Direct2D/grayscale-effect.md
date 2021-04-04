---
title: Efecto de escala de grises
description: Convierte una imagen a gris monocromático.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802629"
---
# <a name="grayscale-effect"></a><span data-ttu-id="6e988-103">Efecto de escala de grises</span><span class="sxs-lookup"><span data-stu-id="6e988-103">Grayscale effect</span></span>

<span data-ttu-id="6e988-104">Convierte una imagen a gris monocromático.</span><span class="sxs-lookup"><span data-stu-id="6e988-104">Converts an image to monochromatic gray.</span></span>

<span data-ttu-id="6e988-105">Escala de grises utiliza el efecto de la matriz de colores para convertir a escala de grises mediante la siguiente matriz:</span><span class="sxs-lookup"><span data-stu-id="6e988-105">Grayscale uses the color matrix effect to convert to grayscale, using the following matrix:</span></span>

![matriz de conversión](images/grayscale-effect-matrix.png)

<span data-ttu-id="6e988-107">El CLSID para este efecto es CLSID \_ D2D1Grayscale.</span><span class="sxs-lookup"><span data-stu-id="6e988-107">The CLSID for this effect is CLSID\_D2D1Grayscale.</span></span>

-   [<span data-ttu-id="6e988-108">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e988-108">Example Image</span></span>](#example-image)
-   [<span data-ttu-id="6e988-109">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="6e988-109">Effect Properties</span></span>](#effect-properties)
-   [<span data-ttu-id="6e988-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e988-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6e988-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e988-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6e988-112">Imagen de ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e988-112">Example image</span></span>

![ejemplo de resultado de efecto](images/grayscale-effect.png)

## <a name="effect-properties"></a><span data-ttu-id="6e988-114">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="6e988-114">Effect properties</span></span>

<span data-ttu-id="6e988-115">Este efecto no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="6e988-115">This effect has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e988-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e988-116">Requirements</span></span>



| <span data-ttu-id="6e988-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e988-117">Requirement</span></span> | <span data-ttu-id="6e988-118">Value</span><span class="sxs-lookup"><span data-stu-id="6e988-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="6e988-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e988-119">Minimum supported client</span></span> | <span data-ttu-id="6e988-120">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="6e988-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6e988-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e988-121">Minimum supported server</span></span> | <span data-ttu-id="6e988-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="6e988-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6e988-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e988-123">Header</span></span>                   | <span data-ttu-id="6e988-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="6e988-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="6e988-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e988-125">Library</span></span>                  | <span data-ttu-id="6e988-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="6e988-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="6e988-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e988-127">Related topics</span></span>

* [<span data-ttu-id="6e988-128">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="6e988-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
