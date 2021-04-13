---
description: Especifica la complejidad del algoritmo del codificador.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: Propiedad MFPKEY_COMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276333"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="7e0ee-103">Propiedad de complejidad de MFPKEY \_</span><span class="sxs-lookup"><span data-stu-id="7e0ee-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="7e0ee-104">\[[**MFPKEY \_ La complejidad**](mfpkey-complexityexproperty.md) está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="7e0ee-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7e0ee-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="7e0ee-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7e0ee-106">En su lugar, use **MFPKEY \_ COMPLEXITYEX**.\]</span><span class="sxs-lookup"><span data-stu-id="7e0ee-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="7e0ee-107">Especifica la complejidad del algoritmo del codificador.</span><span class="sxs-lookup"><span data-stu-id="7e0ee-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7e0ee-108">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7e0ee-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="7e0ee-109">g \_ wszWMVCComplexityMode</span><span class="sxs-lookup"><span data-stu-id="7e0ee-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="7e0ee-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7e0ee-110">Data Type</span></span>

<span data-ttu-id="7e0ee-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7e0ee-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="7e0ee-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7e0ee-112">Default Value</span></span>

<span data-ttu-id="7e0ee-113">El valor predeterminado depende de la versión del codificador de vídeo, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7e0ee-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="7e0ee-114">Versión del codificador</span><span class="sxs-lookup"><span data-stu-id="7e0ee-114">Encoder version</span></span>                 | <span data-ttu-id="7e0ee-115">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7e0ee-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="7e0ee-116">Codificador de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="7e0ee-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="7e0ee-117">3</span><span class="sxs-lookup"><span data-stu-id="7e0ee-117">3</span></span>             |
| <span data-ttu-id="7e0ee-118">Codificador Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="7e0ee-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="7e0ee-119">1</span><span class="sxs-lookup"><span data-stu-id="7e0ee-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="7e0ee-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e0ee-120">Remarks</span></span>

<span data-ttu-id="7e0ee-121">Este valor entero va de 0 a 3.</span><span class="sxs-lookup"><span data-stu-id="7e0ee-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="7e0ee-122">Los valores inferiores hacen que el códec use algoritmos de codificación menos complicados.</span><span class="sxs-lookup"><span data-stu-id="7e0ee-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="7e0ee-123">Aunque los algoritmos más simples producen una salida de menor calidad, el proceso de codificación es más rápido y requiere menos capacidad de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="7e0ee-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e0ee-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e0ee-124">Requirements</span></span>



| <span data-ttu-id="7e0ee-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e0ee-125">Requirement</span></span> | <span data-ttu-id="7e0ee-126">Value</span><span class="sxs-lookup"><span data-stu-id="7e0ee-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0ee-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e0ee-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7e0ee-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7e0ee-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7e0ee-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e0ee-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7e0ee-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e0ee-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7e0ee-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e0ee-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e0ee-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e0ee-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e0ee-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e0ee-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e0ee-134">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e0ee-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




