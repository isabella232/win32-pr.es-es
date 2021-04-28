---
description: 'MFPKEY_COMPLEXITY propiedad : especifica la complejidad del algoritmo del codificador.'
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092943"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="28f01-103">Propiedad MFPKEY \_ COMPLEXITY</span><span class="sxs-lookup"><span data-stu-id="28f01-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="28f01-104">\[[**MFPKEY \_ COMPLEXITY**](mfpkey-complexityexproperty.md) está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.</span><span class="sxs-lookup"><span data-stu-id="28f01-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="28f01-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="28f01-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="28f01-106">En su lugar, use **MFPKEY \_ COMPLEXITYEX**.\]</span><span class="sxs-lookup"><span data-stu-id="28f01-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="28f01-107">Especifica la complejidad del algoritmo del codificador.</span><span class="sxs-lookup"><span data-stu-id="28f01-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="28f01-108">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="28f01-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="28f01-109">g \_ wszWMVCComplexityMode</span><span class="sxs-lookup"><span data-stu-id="28f01-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="28f01-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="28f01-110">Data Type</span></span>

<span data-ttu-id="28f01-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="28f01-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="28f01-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="28f01-112">Default Value</span></span>

<span data-ttu-id="28f01-113">El valor predeterminado depende de la versión del codificador de vídeo, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="28f01-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="28f01-114">Versión del codificador</span><span class="sxs-lookup"><span data-stu-id="28f01-114">Encoder version</span></span>                 | <span data-ttu-id="28f01-115">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="28f01-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="28f01-116">Windows Media Video 9 codificador</span><span class="sxs-lookup"><span data-stu-id="28f01-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="28f01-117">3</span><span class="sxs-lookup"><span data-stu-id="28f01-117">3</span></span>             |
| <span data-ttu-id="28f01-118">Windows Media Video codificador 7/8</span><span class="sxs-lookup"><span data-stu-id="28f01-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="28f01-119">1</span><span class="sxs-lookup"><span data-stu-id="28f01-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="28f01-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28f01-120">Remarks</span></span>

<span data-ttu-id="28f01-121">Este valor entero oscila entre 0 y 3.</span><span class="sxs-lookup"><span data-stu-id="28f01-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="28f01-122">Los valores más bajos hacen que el códec use algoritmos de codificación menos complicados.</span><span class="sxs-lookup"><span data-stu-id="28f01-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="28f01-123">Aunque los algoritmos más sencillos generan resultados de menor calidad, el proceso de codificación es más rápido y requiere menos potencia de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="28f01-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="28f01-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28f01-124">Requirements</span></span>



| <span data-ttu-id="28f01-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="28f01-125">Requirement</span></span> | <span data-ttu-id="28f01-126">Valor</span><span class="sxs-lookup"><span data-stu-id="28f01-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28f01-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28f01-127">Minimum supported client</span></span><br/> | <span data-ttu-id="28f01-128">Solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="28f01-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="28f01-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28f01-129">Minimum supported server</span></span><br/> | <span data-ttu-id="28f01-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="28f01-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28f01-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28f01-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="28f01-132"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="28f01-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28f01-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28f01-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28f01-134">Media Foundation propiedades</span><span class="sxs-lookup"><span data-stu-id="28f01-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




