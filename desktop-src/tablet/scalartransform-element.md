---
description: Transformación escalar usada por drawing o InkWord.
ms.assetid: 88fc3b90-9ec6-41c0-9267-ed5b585ea07b
title: Elemento ScalarTransform
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ed5f7d3b44456522b45c7243b15390b7c52433
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432437"
---
# <a name="scalartransform-element"></a><span data-ttu-id="02719-103">Elemento ScalarTransform</span><span class="sxs-lookup"><span data-stu-id="02719-103">ScalarTransform Element</span></span>

<span data-ttu-id="02719-104">Transformación escalar utilizada por [**drawing**](drawing-element.md) o [**InkWord.**](inkword-element.md)</span><span class="sxs-lookup"><span data-stu-id="02719-104">Scalar transform used by the [**Drawing**](drawing-element.md) or [**InkWord**](inkword-element.md).</span></span>

## <a name="definition"></a><span data-ttu-id="02719-105">Definición</span><span class="sxs-lookup"><span data-stu-id="02719-105">Definition</span></span>

``` syntax
<xs:element name="ScalarTransform" minOccurs="0" type="ScalarTransformType" />
```

## <a name="parent-elements"></a><span data-ttu-id="02719-106">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="02719-106">Parent Elements</span></span>

[<span data-ttu-id="02719-107">**Dibujo**</span><span class="sxs-lookup"><span data-stu-id="02719-107">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="02719-108">**InkWord**</span><span class="sxs-lookup"><span data-stu-id="02719-108">**InkWord**</span></span>](inkword-element.md)

## <a name="child-elements"></a><span data-ttu-id="02719-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02719-109">Child Elements</span></span>

<span data-ttu-id="02719-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="02719-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="02719-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="02719-111">Attributes</span></span>



| <span data-ttu-id="02719-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="02719-112">Attribute</span></span> | <span data-ttu-id="02719-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="02719-113">Type</span></span>           | <span data-ttu-id="02719-114">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-114">Required</span></span> | <span data-ttu-id="02719-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="02719-115">Description</span></span> | <span data-ttu-id="02719-116">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="02719-116">Possible Values</span></span>     |
|-----------|----------------|----------|-------------|---------------------|
| <span data-ttu-id="02719-117">**Mat1**</span><span class="sxs-lookup"><span data-stu-id="02719-117">**Mat1**</span></span>  | <span data-ttu-id="02719-118">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="02719-118">**xs:decimal**</span></span> | <span data-ttu-id="02719-119">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-119">Required</span></span> |             | <span data-ttu-id="02719-120">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="02719-120">Any decimal number.</span></span> |
| <span data-ttu-id="02719-121">**Mat2**</span><span class="sxs-lookup"><span data-stu-id="02719-121">**Mat2**</span></span>  | <span data-ttu-id="02719-122">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="02719-122">**xs:decimal**</span></span> | <span data-ttu-id="02719-123">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-123">Required</span></span> |             | <span data-ttu-id="02719-124">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="02719-124">Any decimal number.</span></span> |
| <span data-ttu-id="02719-125">**Mat3**</span><span class="sxs-lookup"><span data-stu-id="02719-125">**Mat3**</span></span>  | <span data-ttu-id="02719-126">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="02719-126">**xs:decimal**</span></span> | <span data-ttu-id="02719-127">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-127">Required</span></span> |             | <span data-ttu-id="02719-128">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="02719-128">Any decimal number.</span></span> |
| <span data-ttu-id="02719-129">**Mat4**</span><span class="sxs-lookup"><span data-stu-id="02719-129">**Mat4**</span></span>  | <span data-ttu-id="02719-130">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="02719-130">**xs:decimal**</span></span> | <span data-ttu-id="02719-131">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-131">Required</span></span> |             | <span data-ttu-id="02719-132">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="02719-132">Any decimal number.</span></span> |
| <span data-ttu-id="02719-133">**Mat5**</span><span class="sxs-lookup"><span data-stu-id="02719-133">**Mat5**</span></span>  | <span data-ttu-id="02719-134">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="02719-134">**xs:decimal**</span></span> | <span data-ttu-id="02719-135">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-135">Required</span></span> |             | <span data-ttu-id="02719-136">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="02719-136">Any decimal number.</span></span> |
| <span data-ttu-id="02719-137">**Mat6**</span><span class="sxs-lookup"><span data-stu-id="02719-137">**Mat6**</span></span>  | <span data-ttu-id="02719-138">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="02719-138">**xs:decimal**</span></span> | <span data-ttu-id="02719-139">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-139">Required</span></span> |             | <span data-ttu-id="02719-140">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="02719-140">Any decimal number.</span></span> |
| <span data-ttu-id="02719-141">**Mat7**</span><span class="sxs-lookup"><span data-stu-id="02719-141">**Mat7**</span></span>  | <span data-ttu-id="02719-142">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="02719-142">**xs:decimal**</span></span> | <span data-ttu-id="02719-143">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-143">Required</span></span> |             | <span data-ttu-id="02719-144">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="02719-144">Any decimal number.</span></span> |
| <span data-ttu-id="02719-145">**Mat8**</span><span class="sxs-lookup"><span data-stu-id="02719-145">**Mat8**</span></span>  | <span data-ttu-id="02719-146">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="02719-146">**xs:decimal**</span></span> | <span data-ttu-id="02719-147">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-147">Required</span></span> |             | <span data-ttu-id="02719-148">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="02719-148">Any decimal number.</span></span> |
| <span data-ttu-id="02719-149">**Mat9**</span><span class="sxs-lookup"><span data-stu-id="02719-149">**Mat9**</span></span>  | <span data-ttu-id="02719-150">**xs:decimal**</span><span class="sxs-lookup"><span data-stu-id="02719-150">**xs:decimal**</span></span> | <span data-ttu-id="02719-151">Requerido</span><span class="sxs-lookup"><span data-stu-id="02719-151">Required</span></span> |             | <span data-ttu-id="02719-152">Cualquier número decimal.</span><span class="sxs-lookup"><span data-stu-id="02719-152">Any decimal number.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="02719-153">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="02719-153">Element Information</span></span>



| <span data-ttu-id="02719-154">Elemento</span><span class="sxs-lookup"><span data-stu-id="02719-154">Element</span></span>      | <span data-ttu-id="02719-155">Value</span><span class="sxs-lookup"><span data-stu-id="02719-155">Value</span></span>                                                                       |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="02719-156">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="02719-156">Element type</span></span> | <span data-ttu-id="02719-157">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="02719-157">[**ScalarTransformType**](scalartransformtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="02719-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="02719-158">Namespace</span></span>    | <span data-ttu-id="02719-159">urn:schemas-microsoft-com:tabletpc:richink</span><span class="sxs-lookup"><span data-stu-id="02719-159">urn:schemas-microsoft-com:tabletpc:richink</span></span>                                  |
| <span data-ttu-id="02719-160">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="02719-160">Schema name</span></span>  | <span data-ttu-id="02719-161">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="02719-161">Journal Reader</span></span>                                                              |



 

 

 



