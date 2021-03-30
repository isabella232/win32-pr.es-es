---
description: Proporciona información (x, y) de los puntos inicial y final de la línea de base de un párrafo en el documento de diario. El espacio de coordenadas usado para estos valores es HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Elemento Baseline
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275186"
---
# <a name="baseline-element"></a><span data-ttu-id="6e66b-104">Elemento Baseline</span><span class="sxs-lookup"><span data-stu-id="6e66b-104">Baseline Element</span></span>

<span data-ttu-id="6e66b-105">Proporciona información (x, y) de los puntos inicial y final de la línea de base de un párrafo en el documento de diario.</span><span class="sxs-lookup"><span data-stu-id="6e66b-105">Provides (x, y) information for the starting and ending points of the baseline of a paragraph in the Journal document.</span></span> <span data-ttu-id="6e66b-106">El espacio de coordenadas usado para estos valores es **HIMETRIC**.</span><span class="sxs-lookup"><span data-stu-id="6e66b-106">The coordinate space used for these values is **HIMETRIC**.</span></span>

## <a name="definition"></a><span data-ttu-id="6e66b-107">Definición</span><span class="sxs-lookup"><span data-stu-id="6e66b-107">Definition</span></span>

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a><span data-ttu-id="6e66b-108">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="6e66b-108">Parent Elements</span></span>

[<span data-ttu-id="6e66b-109">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="6e66b-109">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="child-elements"></a><span data-ttu-id="6e66b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6e66b-110">Child Elements</span></span>

<span data-ttu-id="6e66b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6e66b-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="6e66b-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e66b-112">Attributes</span></span>



| <span data-ttu-id="6e66b-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="6e66b-113">Attribute</span></span>  | <span data-ttu-id="6e66b-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e66b-114">Type</span></span>                      | <span data-ttu-id="6e66b-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e66b-115">Required</span></span> | <span data-ttu-id="6e66b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e66b-116">Description</span></span>                                                      | <span data-ttu-id="6e66b-117">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6e66b-117">Possible Values</span></span>           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="6e66b-118">**StartX**</span><span class="sxs-lookup"><span data-stu-id="6e66b-118">**StartX**</span></span> | <span data-ttu-id="6e66b-119">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e66b-119">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e66b-120">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e66b-120">Required</span></span> | <span data-ttu-id="6e66b-121">Valor X del punto que marca el principio de la línea base.</span><span class="sxs-lookup"><span data-stu-id="6e66b-121">The X value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="6e66b-122">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="6e66b-122">Any non-negative integer.</span></span> |
| <span data-ttu-id="6e66b-123">**Inicio**</span><span class="sxs-lookup"><span data-stu-id="6e66b-123">**StartY**</span></span> | <span data-ttu-id="6e66b-124">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e66b-124">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e66b-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e66b-125">Required</span></span> | <span data-ttu-id="6e66b-126">Valor Y para el punto que marca el principio de la línea base.</span><span class="sxs-lookup"><span data-stu-id="6e66b-126">The Y value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="6e66b-127">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="6e66b-127">Any non-negative integer.</span></span> |
| <span data-ttu-id="6e66b-128">**EndX**</span><span class="sxs-lookup"><span data-stu-id="6e66b-128">**EndX**</span></span>   | <span data-ttu-id="6e66b-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="6e66b-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="6e66b-130">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="6e66b-130">Required</span></span> | <span data-ttu-id="6e66b-131">Valor X del punto que marca el final de la línea base.</span><span class="sxs-lookup"><span data-stu-id="6e66b-131">The X value for the point marking the end of the baseline.</span></span>       | <span data-ttu-id="6e66b-132">Cualquier entero no negativo.</span><span class="sxs-lookup"><span data-stu-id="6e66b-132">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="6e66b-133">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="6e66b-133">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="6e66b-134">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6e66b-134">Element type</span></span> | <span data-ttu-id="6e66b-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="6e66b-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="6e66b-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e66b-136">Namespace</span></span>    | <span data-ttu-id="6e66b-137">urn: schemas-microsoft-com: TabletPC: richink</span><span class="sxs-lookup"><span data-stu-id="6e66b-137">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="6e66b-138">Nombre del esquema</span><span class="sxs-lookup"><span data-stu-id="6e66b-138">Schema name</span></span>  | <span data-ttu-id="6e66b-139">Lector de diario</span><span class="sxs-lookup"><span data-stu-id="6e66b-139">Journal Reader</span></span>                                                |



 

 

 



