---
description: Efecto del establecedor alfa
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Efecto del establecedor alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805929"
---
# <a name="alpha-setter-effect"></a><span data-ttu-id="a6bdb-103">Efecto del establecedor alfa</span><span class="sxs-lookup"><span data-stu-id="a6bdb-103">Alpha Setter Effect</span></span>

> [!Note]  
> <span data-ttu-id="a6bdb-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a6bdb-104">\[Deprecated.</span></span> <span data-ttu-id="a6bdb-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a6bdb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a6bdb-106">El efecto establecedor alfa establece los bits alfa de una imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a6bdb-106">The Alpha Setter effect sets the alpha bits on a video image.</span></span>

<span data-ttu-id="a6bdb-107">IDENTIFICADOR de clase (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span><span class="sxs-lookup"><span data-stu-id="a6bdb-107">Class ID (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}</span></span>

<span data-ttu-id="a6bdb-108">Nombre de la variable CLSID: CLSID \_ DxtAlphaSetter</span><span class="sxs-lookup"><span data-stu-id="a6bdb-108">CLSID Variable Name: CLSID\_DxtAlphaSetter</span></span>

<span data-ttu-id="a6bdb-109">Nombre descriptivo: "DxtAlphaSetter"</span><span class="sxs-lookup"><span data-stu-id="a6bdb-109">Friendly Name: "DxtAlphaSetter"</span></span>

### <a name="properties"></a><span data-ttu-id="a6bdb-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a6bdb-110">Properties</span></span>



| <span data-ttu-id="a6bdb-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a6bdb-111">Property</span></span>  | <span data-ttu-id="a6bdb-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6bdb-112">Type</span></span>   | <span data-ttu-id="a6bdb-113">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a6bdb-113">Default</span></span> | <span data-ttu-id="a6bdb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6bdb-114">Description</span></span>                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| <span data-ttu-id="a6bdb-115">Alpha</span><span class="sxs-lookup"><span data-stu-id="a6bdb-115">Alpha</span></span>     | <span data-ttu-id="a6bdb-116">BYTE</span><span class="sxs-lookup"><span data-stu-id="a6bdb-116">BYTE</span></span>   | <span data-ttu-id="a6bdb-117">-1</span><span class="sxs-lookup"><span data-stu-id="a6bdb-117">-1</span></span>      | <span data-ttu-id="a6bdb-118">Establece el alfa de la imagen completa.</span><span class="sxs-lookup"><span data-stu-id="a6bdb-118">Sets the alpha for the entire image.</span></span>                        |
| <span data-ttu-id="a6bdb-119">AlphaRamp</span><span class="sxs-lookup"><span data-stu-id="a6bdb-119">AlphaRamp</span></span> | <span data-ttu-id="a6bdb-120">double</span><span class="sxs-lookup"><span data-stu-id="a6bdb-120">double</span></span> | <span data-ttu-id="a6bdb-121">-1.0</span><span class="sxs-lookup"><span data-stu-id="a6bdb-121">-1.0</span></span>    | <span data-ttu-id="a6bdb-122">Establece el alfa como porcentaje del valor alfa original.</span><span class="sxs-lookup"><span data-stu-id="a6bdb-122">Sets the alpha as a percentage of the original alpha value.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a6bdb-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6bdb-123">Remarks</span></span>

<span data-ttu-id="a6bdb-124">Se omite una propiedad con un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="a6bdb-124">A property with a negative value is ignored.</span></span> <span data-ttu-id="a6bdb-125">Solo una propiedad puede tener un valor no negativo.</span><span class="sxs-lookup"><span data-stu-id="a6bdb-125">Only one property can have a non-negative value.</span></span> <span data-ttu-id="a6bdb-126">La propiedad alfa especifica un valor alfa constante para cada píxel de la imagen.</span><span class="sxs-lookup"><span data-stu-id="a6bdb-126">The Alpha property specifies a constant alpha value for every pixel in the image.</span></span> <span data-ttu-id="a6bdb-127">Esta propiedad sobrescribe los valores alfa de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="a6bdb-127">This property overwrites the alpha values from the original image.</span></span> <span data-ttu-id="a6bdb-128">La propiedad AlphaRamp especifica el valor alfa de cada píxel como un porcentaje del valor original del píxel, de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="a6bdb-128">The AlphaRamp property specifies each pixel's alpha value as a percentage of the pixel's original value, from 0.0 to 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6bdb-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a6bdb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6bdb-130">Combinación alfa</span><span class="sxs-lookup"><span data-stu-id="a6bdb-130">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



