---
description: El método GetTitleParentalLevels recupera los niveles de administración parentales para el título especificado.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Método GetTitleParentalLevels
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422899"
---
# <a name="gettitleparentallevels-method"></a><span data-ttu-id="c7581-103">Método GetTitleParentalLevels</span><span class="sxs-lookup"><span data-stu-id="c7581-103">GetTitleParentalLevels Method</span></span>

> [!Note]  
> <span data-ttu-id="c7581-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c7581-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c7581-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="c7581-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c7581-106">El `GetTitleParentalLevels` método recupera los niveles de administración parentales para el título especificado.</span><span class="sxs-lookup"><span data-stu-id="c7581-106">The `GetTitleParentalLevels` method retrieves the parental management levels for the specified title.</span></span>

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a><span data-ttu-id="c7581-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7581-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7581-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="c7581-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="c7581-109">Especifica el título como un entero.</span><span class="sxs-lookup"><span data-stu-id="c7581-109">Specifies the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7581-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7581-110">Return Value</span></span>

<span data-ttu-id="c7581-111">Devuelve un valor entero cuyos bits individuales indican qué niveles de administración parentales (PML) están establecidos en el título especificado.</span><span class="sxs-lookup"><span data-stu-id="c7581-111">Returns an integer value whose individual bits indicate which parental management levels (PML) are set in the specified title.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7581-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7581-112">Remarks</span></span>

<span data-ttu-id="c7581-113">Un título puede tener capítulos o incluso segmentos cortos que tengan un PML diferente del PML general para el título.</span><span class="sxs-lookup"><span data-stu-id="c7581-113">A title may have chapters or even short segments that have a PML different from the overall PML for the title.</span></span> <span data-ttu-id="c7581-114">Use este método para determinar todas las PMLs que se detectarán al reproducir un título especificado.</span><span class="sxs-lookup"><span data-stu-id="c7581-114">Use this method to determine all the PMLs that will be encountered when playing a specified title.</span></span> <span data-ttu-id="c7581-115">El entero devuelto es un conjunto de marcadores de bits que se definen como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7581-115">The returned integer is a set of bit flags that are defined as shown in the table below.</span></span> <span data-ttu-id="c7581-116">Realice una operación and bit a bit en *iLevels* y cada valor posible.</span><span class="sxs-lookup"><span data-stu-id="c7581-116">Perform a bitwise AND operation on *iLevels* and each possible value.</span></span> <span data-ttu-id="c7581-117">Si la operación devuelve **true**, significa que PML se encontrará en algún punto de este título.</span><span class="sxs-lookup"><span data-stu-id="c7581-117">If the operation returns **true**, it means that PML will be encountered at some point in this title.</span></span>



| <span data-ttu-id="c7581-118">Value</span><span class="sxs-lookup"><span data-stu-id="c7581-118">Value</span></span>  | <span data-ttu-id="c7581-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7581-119">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="c7581-120">0x100</span><span class="sxs-lookup"><span data-stu-id="c7581-120">0x100</span></span>  | <span data-ttu-id="c7581-121">Nivel parental de DVD 1</span><span class="sxs-lookup"><span data-stu-id="c7581-121">DVD Parental Level 1</span></span> |
| <span data-ttu-id="c7581-122">0x200</span><span class="sxs-lookup"><span data-stu-id="c7581-122">0x200</span></span>  | <span data-ttu-id="c7581-123">Nivel parental de DVD 2</span><span class="sxs-lookup"><span data-stu-id="c7581-123">DVD Parental Level 2</span></span> |
| <span data-ttu-id="c7581-124">0x400</span><span class="sxs-lookup"><span data-stu-id="c7581-124">0x400</span></span>  | <span data-ttu-id="c7581-125">Nivel parental de DVD 3</span><span class="sxs-lookup"><span data-stu-id="c7581-125">DVD Parental Level 3</span></span> |
| <span data-ttu-id="c7581-126">0x800</span><span class="sxs-lookup"><span data-stu-id="c7581-126">0x800</span></span>  | <span data-ttu-id="c7581-127">DVD de nivel superior 4</span><span class="sxs-lookup"><span data-stu-id="c7581-127">DVD Parental Level 4</span></span> |
| <span data-ttu-id="c7581-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="c7581-128">0x1000</span></span> | <span data-ttu-id="c7581-129">Nivel parental de DVD 5</span><span class="sxs-lookup"><span data-stu-id="c7581-129">DVD Parental Level 5</span></span> |
| <span data-ttu-id="c7581-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="c7581-130">0x2000</span></span> | <span data-ttu-id="c7581-131">Nivel parental de DVD 6</span><span class="sxs-lookup"><span data-stu-id="c7581-131">DVD Parental Level 6</span></span> |
| <span data-ttu-id="c7581-132">0x4000</span><span class="sxs-lookup"><span data-stu-id="c7581-132">0x4000</span></span> | <span data-ttu-id="c7581-133">Nivel parental de DVD 7</span><span class="sxs-lookup"><span data-stu-id="c7581-133">DVD Parental Level 7</span></span> |
| <span data-ttu-id="c7581-134">0x8000</span><span class="sxs-lookup"><span data-stu-id="c7581-134">0x8000</span></span> | <span data-ttu-id="c7581-135">Nivel parental de DVD 8</span><span class="sxs-lookup"><span data-stu-id="c7581-135">DVD Parental Level 8</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="c7581-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7581-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7581-137">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="c7581-137">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="c7581-138">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="c7581-138">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="c7581-139">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="c7581-139">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="c7581-140">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="c7581-140">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 



