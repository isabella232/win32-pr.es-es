---
title: Efecto de máscara alfa
description: Este efecto aplica una máscara alfa a una imagen. Tiene dos entradas, denominadas Destination y Mask. Los valores de color de la imagen de destino se multiplican por el canal alfa de la imagen de máscara.
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87669608ab75ab7a655c072e174dbcd19df4bb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151246"
---
# <a name="alpha-mask-effect"></a><span data-ttu-id="4fcd8-105">Efecto de máscara alfa</span><span class="sxs-lookup"><span data-stu-id="4fcd8-105">Alpha mask effect</span></span>

<span data-ttu-id="4fcd8-106">Este efecto aplica una máscara alfa a una imagen.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-106">This effect applies an alpha mask to an image.</span></span> <span data-ttu-id="4fcd8-107">Tiene dos entradas, denominadas Destination y Mask.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-107">It has two inputs, named Destination and Mask.</span></span> <span data-ttu-id="4fcd8-108">Los valores de color de la imagen de destino se multiplican por el canal alfa de la imagen de máscara.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-108">Color values in the Destination image are multiplied by the alpha channel of the Mask image.</span></span>

<span data-ttu-id="4fcd8-109">El CLSID para este efecto es CLSID \_ D2D1AlphaMask.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-109">The CLSID for this effect is CLSID\_D2D1AlphaMask.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="4fcd8-110">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="4fcd8-110">Effect properties</span></span>

<span data-ttu-id="4fcd8-111">Este efecto no tiene propiedades específicas del efecto.</span><span class="sxs-lookup"><span data-stu-id="4fcd8-111">This effect has no effect-specific properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fcd8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fcd8-112">Requirements</span></span>



| <span data-ttu-id="4fcd8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fcd8-113">Requirement</span></span> | <span data-ttu-id="4fcd8-114">Value</span><span class="sxs-lookup"><span data-stu-id="4fcd8-114">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="4fcd8-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fcd8-115">Minimum supported client</span></span> | <span data-ttu-id="4fcd8-116">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="4fcd8-116">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4fcd8-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fcd8-117">Minimum supported server</span></span> | <span data-ttu-id="4fcd8-118">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="4fcd8-118">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="4fcd8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fcd8-119">Header</span></span>                   | <span data-ttu-id="4fcd8-120">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="4fcd8-120">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="4fcd8-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4fcd8-121">Library</span></span>                  | <span data-ttu-id="4fcd8-122">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="4fcd8-122">d2d1.lib, dxguid.lib</span></span>                              |

## <a name="related-topics"></a><span data-ttu-id="4fcd8-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4fcd8-123">Related topics</span></span>

* [<span data-ttu-id="4fcd8-124">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="4fcd8-124">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

