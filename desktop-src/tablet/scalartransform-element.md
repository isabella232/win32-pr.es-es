---
description: Transformación escalar utilizada por el dibujo o InkWord.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Elemento ScalarTransform
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5853c0fab76cd5a4857ae0235127a2fe103872
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716715"
---
# <a name="scalartransform-element"></a><span data-ttu-id="fef17-103">Elemento ScalarTransform</span><span class="sxs-lookup"><span data-stu-id="fef17-103">ScalarTransform Element</span></span>

<span data-ttu-id="fef17-104">Transformación escalar utilizada por el [**dibujo**](drawing-element.md) o [**InkWord**](inkword-element.md).</span><span class="sxs-lookup"><span data-stu-id="fef17-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="fef17-105">Definición</span><span class="sxs-lookup"><span data-stu-id="fef17-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="fef17-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="fef17-106">Parent Elements</span></span>

[<span data-ttu-id="fef17-107">**Dibujo**</span><span class="sxs-lookup"><span data-stu-id="fef17-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="fef17-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="fef17-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="fef17-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fef17-109">Child Elements</span></span>

<span data-ttu-id="fef17-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fef17-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="fef17-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="fef17-111">Attributes</span></span>



| <span data-ttu-id="fef17-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="fef17-112">Attribute</span></span> | <span data-ttu-id="fef17-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="fef17-113">Type</span></span>           | <span data-ttu-id="fef17-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-114">Required</span></span> | <span data-ttu-id="fef17-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="fef17-115">Description</span></span> | <span data-ttu-id="fef17-116">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="fef17-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="fef17-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="fef17-117">**Mat1**</span></span>  | <span data-ttu-id="fef17-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="fef17-118">**xs:decimal**</span></span> | <span data-ttu-id="fef17-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-119">Required</span></span> |             | <span data-ttu-id="fef17-120">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="fef17-120">Any decimal number.</span></span> |
| <span data-ttu-id="fef17-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="fef17-121">**Mat2**</span></span>  | <span data-ttu-id="fef17-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="fef17-122">**xs:decimal**</span></span> | <span data-ttu-id="fef17-123">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-123">Required</span></span> |             | <span data-ttu-id="fef17-124">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="fef17-124">Any decimal number.</span></span> |
| <span data-ttu-id="fef17-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="fef17-125">**Mat3**</span></span>  | <span data-ttu-id="fef17-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="fef17-126">**xs:decimal**</span></span> | <span data-ttu-id="fef17-127">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-127">Required</span></span> |             | <span data-ttu-id="fef17-128">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="fef17-128">Any decimal number.</span></span> |
| <span data-ttu-id="fef17-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="fef17-129">**Mat4**</span></span>  | <span data-ttu-id="fef17-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="fef17-130">**xs:decimal**</span></span> | <span data-ttu-id="fef17-131">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-131">Required</span></span> |             | <span data-ttu-id="fef17-132">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="fef17-132">Any decimal number.</span></span> |
| <span data-ttu-id="fef17-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="fef17-133">**Mat5**</span></span>  | <span data-ttu-id="fef17-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="fef17-134">**xs:decimal**</span></span> | <span data-ttu-id="fef17-135">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-135">Required</span></span> |             | <span data-ttu-id="fef17-136">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="fef17-136">Any decimal number.</span></span> |
| <span data-ttu-id="fef17-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="fef17-137">**Mat6**</span></span>  | <span data-ttu-id="fef17-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="fef17-138">**xs:decimal**</span></span> | <span data-ttu-id="fef17-139">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-139">Required</span></span> |             | <span data-ttu-id="fef17-140">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="fef17-140">Any decimal number.</span></span> |
| <span data-ttu-id="fef17-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="fef17-141">**Mat7**</span></span>  | <span data-ttu-id="fef17-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="fef17-142">**xs:decimal**</span></span> | <span data-ttu-id="fef17-143">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-143">Required</span></span> |             | <span data-ttu-id="fef17-144">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="fef17-144">Any decimal number.</span></span> |
| <span data-ttu-id="fef17-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="fef17-145">**Mat8**</span></span>  | <span data-ttu-id="fef17-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="fef17-146">**xs:decimal**</span></span> | <span data-ttu-id="fef17-147">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-147">Required</span></span> |             | <span data-ttu-id="fef17-148">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="fef17-148">Any decimal number.</span></span> |
| <span data-ttu-id="fef17-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="fef17-149">**Mat9**</span></span>  | <span data-ttu-id="fef17-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="fef17-150">**xs:decimal**</span></span> | <span data-ttu-id="fef17-151">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fef17-151">Required</span></span> |             | <span data-ttu-id="fef17-152">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="fef17-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="fef17-153">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="fef17-153">Element Information</span></span>



|              |                                                                             |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="fef17-154">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="fef17-154">Element type</span></span> | <span data-ttu-id="fef17-155">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="fef17-155">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="fef17-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fef17-156">Namespace</span></span>    | <span data-ttu-id="fef17-157">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="fef17-157">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="fef17-158">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="fef17-158">Schema name</span></span>  | <span data-ttu-id="fef17-159">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="fef17-159">Journal Reader</span></span>                                                              |



 

 

 



