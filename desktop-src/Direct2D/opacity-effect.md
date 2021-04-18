---
title: Efecto opacidad
description: Este efecto ajusta la opacidad de una imagen multiplicando el canal alfa de la entrada por el valor de opacidad especificado. Tiene una sola entrada.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686092"
---
# <a name="opacity-effect"></a><span data-ttu-id="87a7f-104">Efecto opacidad</span><span class="sxs-lookup"><span data-stu-id="87a7f-104">Opacity effect</span></span>

<span data-ttu-id="87a7f-105">Este efecto ajusta la opacidad de una imagen multiplicando el canal alfa de la entrada por el valor de opacidad especificado.</span><span class="sxs-lookup"><span data-stu-id="87a7f-105">This effect adjusts the opacity of an image by multiplying the alpha channel of the input by the specified opacity value.</span></span> <span data-ttu-id="87a7f-106">Tiene una sola entrada.</span><span class="sxs-lookup"><span data-stu-id="87a7f-106">It has a single input.</span></span>

<span data-ttu-id="87a7f-107">El CLSID para este efecto es CLSID \_ D2D1Opacity.</span><span class="sxs-lookup"><span data-stu-id="87a7f-107">The CLSID for this effect is CLSID\_D2D1Opacity.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="87a7f-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="87a7f-108">Effect properties</span></span>



| <span data-ttu-id="87a7f-109">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="87a7f-109">Display name and index enumeration</span></span>              | <span data-ttu-id="87a7f-110">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="87a7f-110">Type and default value</span></span> | <span data-ttu-id="87a7f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="87a7f-111">Description</span></span>                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a7f-112">Opacidad D2D1 opacidad opacidad \_ \_ prop. \_</span><span class="sxs-lookup"><span data-stu-id="87a7f-112">Opacity D2D1\_OPACITY\_PROP\_OPACITY</span></span><br/> | <span data-ttu-id="87a7f-113">FLOAT 1.0 f</span><span class="sxs-lookup"><span data-stu-id="87a7f-113">FLOAT1.0f</span></span><br/>   | <span data-ttu-id="87a7f-114">Multiplicador del canal alfa de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="87a7f-114">The multiplier to the input image's alpha channel.</span></span> <span data-ttu-id="87a7f-115">El valor mínimo es 0,0 f y el valor máximo es 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="87a7f-115">The minimum value is 0.0f and the maximum value is 1.0f.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="87a7f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87a7f-116">Requirements</span></span>



| <span data-ttu-id="87a7f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="87a7f-117">Requirement</span></span> | <span data-ttu-id="87a7f-118">Value</span><span class="sxs-lookup"><span data-stu-id="87a7f-118">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="87a7f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87a7f-119">Minimum supported client</span></span> | <span data-ttu-id="87a7f-120">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="87a7f-120">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="87a7f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87a7f-121">Minimum supported server</span></span> | <span data-ttu-id="87a7f-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="87a7f-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="87a7f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87a7f-123">Header</span></span>                   | <span data-ttu-id="87a7f-124">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="87a7f-124">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="87a7f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87a7f-125">Library</span></span>                  | <span data-ttu-id="87a7f-126">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="87a7f-126">d2d1.lib, dxguid.lib</span></span>                              |


## <a name="related-topics"></a><span data-ttu-id="87a7f-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87a7f-127">Related topics</span></span>

* [<span data-ttu-id="87a7f-128">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="87a7f-128">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
