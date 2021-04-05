---
title: Efecto de matiz
description: Este efecto tiñe la imagen de origen multiplicando la imagen de origen por el color especificado. Tiene una sola entrada.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996321"
---
# <a name="tint-effect"></a><span data-ttu-id="741e3-104">Efecto de matiz</span><span class="sxs-lookup"><span data-stu-id="741e3-104">Tint effect</span></span>

<span data-ttu-id="741e3-105">Este efecto tiñe la imagen de origen multiplicando la imagen de origen por el color especificado.</span><span class="sxs-lookup"><span data-stu-id="741e3-105">This effect tints the source image by multiplying the source image by the specified color.</span></span> <span data-ttu-id="741e3-106">Tiene una sola entrada.</span><span class="sxs-lookup"><span data-stu-id="741e3-106">It has a single input.</span></span>

<span data-ttu-id="741e3-107">El CLSID para este efecto es CLSID \_ D2D1Tint.</span><span class="sxs-lookup"><span data-stu-id="741e3-107">The CLSID for this effect is CLSID\_D2D1Tint.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="741e3-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="741e3-108">Effect properties</span></span>



| <span data-ttu-id="741e3-109">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="741e3-109">Display name and index enumeration</span></span>                    | <span data-ttu-id="741e3-110">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="741e3-110">Type and default value</span></span>                              | <span data-ttu-id="741e3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="741e3-111">Description</span></span>                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="741e3-112">COLOR de la ColorD2D1 de \_ tinte \_ \_</span><span class="sxs-lookup"><span data-stu-id="741e3-112">ColorD2D1\_TINT\_PROP\_COLOR</span></span><br/>               | <span data-ttu-id="741e3-113">D2D1 \_ Vector \_ 4F (1.0 f, 1.0 f, 1.0 f, 1.0 f)</span><span class="sxs-lookup"><span data-stu-id="741e3-113">D2D1\_VECTOR\_4F(1.0f, 1.0f, 1.0f, 1.0f)</span></span><br/> | <span data-ttu-id="741e3-114">Los colores de la imagen de origen se multiplican por este valor.</span><span class="sxs-lookup"><span data-stu-id="741e3-114">Colors from the source image are multiplied by this value.</span></span>       |
| <span data-ttu-id="741e3-115">Salida de la abrazadera de propiedades de \_ matiz ClampOutputD2D1 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="741e3-115">ClampOutputD2D1\_TINT\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="741e3-116">BOOLFALSE</span><span class="sxs-lookup"><span data-stu-id="741e3-116">BOOLFALSE</span></span><br/>                                | <span data-ttu-id="741e3-117">Indica si se deben fijar o no los valores de salida en el intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="741e3-117">Whether or not to clamp the output values to the range \[0, 1\].</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="741e3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="741e3-118">Requirements</span></span>



| <span data-ttu-id="741e3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="741e3-119">Requirement</span></span> | <span data-ttu-id="741e3-120">Value</span><span class="sxs-lookup"><span data-stu-id="741e3-120">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="741e3-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741e3-121">Minimum supported client</span></span> | <span data-ttu-id="741e3-122">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="741e3-122">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="741e3-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="741e3-123">Minimum supported server</span></span> | <span data-ttu-id="741e3-124">Aplicaciones de la tienda Windows de Windows 10 \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="741e3-124">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="741e3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="741e3-125">Header</span></span>                   | <span data-ttu-id="741e3-126">d2d1effects \_ 2. h</span><span class="sxs-lookup"><span data-stu-id="741e3-126">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="741e3-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="741e3-127">Library</span></span>                  | <span data-ttu-id="741e3-128">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="741e3-128">d2d1.lib, dxguid.lib</span></span>                              |



 ## <a name="related-topics"></a><span data-ttu-id="741e3-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="741e3-129">Related topics</span></span>

* [<span data-ttu-id="741e3-130">Interfaz ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="741e3-130">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
