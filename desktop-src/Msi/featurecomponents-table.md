---
description: La tabla FeatureComponents define la relación entre las características y los componentes de. Para cada característica, en esta tabla se enumeran todos los componentes que componen esa característica.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Tabla FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811821"
---
# <a name="featurecomponents-table"></a><span data-ttu-id="377e0-104">Tabla FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="377e0-104">FeatureComponents Table</span></span>

<span data-ttu-id="377e0-105">La tabla FeatureComponents define la relación entre las características y los componentes de.</span><span class="sxs-lookup"><span data-stu-id="377e0-105">The FeatureComponents table defines the relationship between features and components.</span></span> <span data-ttu-id="377e0-106">Para cada característica, en esta tabla se enumeran todos los componentes que componen esa característica.</span><span class="sxs-lookup"><span data-stu-id="377e0-106">For each feature, this table lists all the components that make up that feature.</span></span>

<span data-ttu-id="377e0-107">La tabla FeatureComponents tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="377e0-107">The FeatureComponents table has the following columns.</span></span>



| <span data-ttu-id="377e0-108">Columna</span><span class="sxs-lookup"><span data-stu-id="377e0-108">Column</span></span>      | <span data-ttu-id="377e0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="377e0-109">Type</span></span>                         | <span data-ttu-id="377e0-110">Clave</span><span class="sxs-lookup"><span data-stu-id="377e0-110">Key</span></span> | <span data-ttu-id="377e0-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="377e0-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="377e0-112">Característica\_</span><span class="sxs-lookup"><span data-stu-id="377e0-112">Feature\_</span></span>   | [<span data-ttu-id="377e0-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="377e0-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="377e0-114">Y</span><span class="sxs-lookup"><span data-stu-id="377e0-114">Y</span></span>   | <span data-ttu-id="377e0-115">N</span><span class="sxs-lookup"><span data-stu-id="377e0-115">N</span></span>        |
| <span data-ttu-id="377e0-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="377e0-116">Component\_</span></span> | [<span data-ttu-id="377e0-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="377e0-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="377e0-118">Y</span><span class="sxs-lookup"><span data-stu-id="377e0-118">Y</span></span>   | <span data-ttu-id="377e0-119">N</span><span class="sxs-lookup"><span data-stu-id="377e0-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="377e0-120">Columnas</span><span class="sxs-lookup"><span data-stu-id="377e0-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="377e0-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_</span><span class="sxs-lookup"><span data-stu-id="377e0-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="377e0-122">Una clave externa en la primera columna de la [tabla](feature-table.md)de características.</span><span class="sxs-lookup"><span data-stu-id="377e0-122">An external key into the first column of the Feature [table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="377e0-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="377e0-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="377e0-124">Una clave externa en la primera columna de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="377e0-124">An external key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="377e0-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="377e0-125">Remarks</span></span>

<span data-ttu-id="377e0-126">Existe un límite máximo de 1600 componentes por característica.</span><span class="sxs-lookup"><span data-stu-id="377e0-126">There is a maximum limit of 1600 components per feature.</span></span>

<span data-ttu-id="377e0-127">Dos o más características pueden compartir los componentes, es decir, se puede hacer referencia al mismo componente a través de más de una característica.</span><span class="sxs-lookup"><span data-stu-id="377e0-127">Components can be shared by two or more features, that is, the same component can be referred to by more than one feature.</span></span>

<span data-ttu-id="377e0-128">Se hace referencia a esta tabla cuando se ejecuta la acción [PublishFeatures](publishfeatures-action.md) o la [acción UnpublishFeatures](unpublishfeatures-action.md) .</span><span class="sxs-lookup"><span data-stu-id="377e0-128">This table is referred to when the [PublishFeatures action](publishfeatures-action.md) or the [UnpublishFeatures action](unpublishfeatures-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="377e0-129">Validación</span><span class="sxs-lookup"><span data-stu-id="377e0-129">Validation</span></span>

<dl>

[<span data-ttu-id="377e0-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="377e0-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="377e0-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="377e0-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="377e0-132">ICE21</span><span class="sxs-lookup"><span data-stu-id="377e0-132">ICE21</span></span>](ice21.md)  
[<span data-ttu-id="377e0-133">ICE22</span><span class="sxs-lookup"><span data-stu-id="377e0-133">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="377e0-134">ICE32</span><span class="sxs-lookup"><span data-stu-id="377e0-134">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="377e0-135">ICE41</span><span class="sxs-lookup"><span data-stu-id="377e0-135">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="377e0-136">ICE47</span><span class="sxs-lookup"><span data-stu-id="377e0-136">ICE47</span></span>](ice47.md)  
[<span data-ttu-id="377e0-137">ICE59</span><span class="sxs-lookup"><span data-stu-id="377e0-137">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="377e0-138">ICE62</span><span class="sxs-lookup"><span data-stu-id="377e0-138">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="377e0-139">ICE69</span><span class="sxs-lookup"><span data-stu-id="377e0-139">ICE69</span></span>](ice69.md)  
</dl>

 

 



