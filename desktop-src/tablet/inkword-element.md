---
description: Contiene información sobre una palabra de entrada de lápiz determinada en la nota del diario, incluida la posición, las alternativas y los datos de entrada de lápiz reales.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dc9baea7cda0346e82c11331c45f453e61f192
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432397"
---
# <a name="inkword-element"></a><span data-ttu-id="5c855-103">Elemento InkWord</span><span class="sxs-lookup"><span data-stu-id="5c855-103">InkWord Element</span></span>

<span data-ttu-id="5c855-104">Contiene información sobre una palabra de entrada de lápiz determinada en la nota del diario, incluida la posición, las alternativas y los datos de entrada de lápiz reales.</span><span class="sxs-lookup"><span data-stu-id="5c855-104">Contains information about a given ink word in the Journal note, including position, alternates, and the actual ink data.</span></span>

## <a name="definition"></a><span data-ttu-id="5c855-105">Definición</span><span class="sxs-lookup"><span data-stu-id="5c855-105">Definition</span></span>

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a><span data-ttu-id="5c855-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="5c855-106">Parent Elements</span></span>

[<span data-ttu-id="5c855-107">**GroupNode**</span><span class="sxs-lookup"><span data-stu-id="5c855-107">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="5c855-108">**Línea**</span><span class="sxs-lookup"><span data-stu-id="5c855-108">**Line**</span></span>](line-element.md)

## <a name="child-elements"></a><span data-ttu-id="5c855-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5c855-109">Child Elements</span></span>

[<span data-ttu-id="5c855-110">**ScalarTransform**</span><span class="sxs-lookup"><span data-stu-id="5c855-110">**ScalarTransform**</span></span>](scalartransform-element.md)

[<span data-ttu-id="5c855-111">**AlternateList**</span><span class="sxs-lookup"><span data-stu-id="5c855-111">**AlternateList**</span></span>](alternatelist-element.md)

[<span data-ttu-id="5c855-112">**CanReClassify**</span><span class="sxs-lookup"><span data-stu-id="5c855-112">**CanReClassify**</span></span>](canreclassify-element.md)

[<span data-ttu-id="5c855-113">**Confianza**</span><span class="sxs-lookup"><span data-stu-id="5c855-113">**Confidence**</span></span>](confidence-element.md)

[<span data-ttu-id="5c855-114">**InkObject**</span><span class="sxs-lookup"><span data-stu-id="5c855-114">**InkObject**</span></span>](inkobject-element.md)

## <a name="attributes"></a><span data-ttu-id="5c855-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="5c855-115">Attributes</span></span>



| <span data-ttu-id="5c855-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="5c855-116">Attribute</span></span>  | <span data-ttu-id="5c855-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c855-117">Type</span></span>                      | <span data-ttu-id="5c855-118">Requerido</span><span class="sxs-lookup"><span data-stu-id="5c855-118">Required</span></span> | <span data-ttu-id="5c855-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c855-119">Description</span></span>                                                                             | <span data-ttu-id="5c855-120">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5c855-120">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="5c855-121">**Left**</span><span class="sxs-lookup"><span data-stu-id="5c855-121">**Left**</span></span>   | <span data-ttu-id="5c855-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5c855-122">**xs:integer**</span></span>            | <span data-ttu-id="5c855-123">Requerido</span><span class="sxs-lookup"><span data-stu-id="5c855-123">Required</span></span> | <span data-ttu-id="5c855-124">Distancia desde el origen hasta el punto situado más a la izquierda en el cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="5c855-124">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="5c855-125">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="5c855-125">Any integer.</span></span>              |
| <span data-ttu-id="5c855-126">**Top** (Principales)</span><span class="sxs-lookup"><span data-stu-id="5c855-126">**Top**</span></span>    | <span data-ttu-id="5c855-127">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="5c855-127">**xs:integer**</span></span>            | <span data-ttu-id="5c855-128">Requerido</span><span class="sxs-lookup"><span data-stu-id="5c855-128">Required</span></span> | <span data-ttu-id="5c855-129">Distancia desde el origen hasta el punto superior del cuadro de límite del elemento.</span><span class="sxs-lookup"><span data-stu-id="5c855-129">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="5c855-130">Cualquier número entero.</span><span class="sxs-lookup"><span data-stu-id="5c855-130">Any integer.</span></span>              |
| <span data-ttu-id="5c855-131">**Width**</span><span class="sxs-lookup"><span data-stu-id="5c855-131">**Width**</span></span>  | <span data-ttu-id="5c855-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5c855-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5c855-133">Requerido</span><span class="sxs-lookup"><span data-stu-id="5c855-133">Required</span></span> | <span data-ttu-id="5c855-134">Ancho del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="5c855-134">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="5c855-135">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="5c855-135">Any non-negative integer.</span></span> |
| <span data-ttu-id="5c855-136">**Height**</span><span class="sxs-lookup"><span data-stu-id="5c855-136">**Height**</span></span> | <span data-ttu-id="5c855-137">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="5c855-137">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="5c855-138">Requerido</span><span class="sxs-lookup"><span data-stu-id="5c855-138">Required</span></span> | <span data-ttu-id="5c855-139">Alto del cuadro de límite para el elemento.</span><span class="sxs-lookup"><span data-stu-id="5c855-139">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="5c855-140">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="5c855-140">Any non-negative integer.</span></span> |



 

> [!WARNING]
> <span data-ttu-id="5c855-141">La asignación de coordenadas internas de la palabra manuscrita es Unidades métricas en inglés y la aplicación deberá usar un multiplicador de 2,54 para convertir los valores width y Height en las unidades HIMETRIC que usan las API de la plataforma de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="5c855-141">The ink word's internal coordinate mapping is English Metric Units and a multiplier of 2.54 will need to be used by your application to convert the Width and Height values to the HIMETRIC units used by the Tablet PC platform APIs.</span></span>

 

## <a name="element-information"></a><span data-ttu-id="5c855-142">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="5c855-142">Element Information</span></span>



|  <span data-ttu-id="5c855-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="5c855-143">Element</span></span>     | <span data-ttu-id="5c855-144">Value</span><span class="sxs-lookup"><span data-stu-id="5c855-144">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="5c855-145">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5c855-145">Element type</span></span> | <span data-ttu-id="5c855-146">[**InkWordType**](inkwordtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="5c855-146">[**InkWordType**](inkwordtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="5c855-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5c855-147">Namespace</span></span>    | <span data-ttu-id="5c855-148">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="5c855-148">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="5c855-149">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="5c855-149">Schema name</span></span>  | <span data-ttu-id="5c855-150">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="5c855-150">Journal Reader</span></span>                                              |



 

 

 



