---
description: ICE47 comprueba la característica y las tablas FeatureComponents para ver si hay características con 1600 o más componentes.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276718"
---
# <a name="ice47"></a><span data-ttu-id="6b7c8-103">ICE47</span><span class="sxs-lookup"><span data-stu-id="6b7c8-103">ICE47</span></span>

<span data-ttu-id="6b7c8-104">ICE47 comprueba la [característica](feature-table.md) y las tablas [FeatureComponents](featurecomponents-table.md) para ver si hay características con 1600 o más componentes.</span><span class="sxs-lookup"><span data-stu-id="6b7c8-104">ICE47 checks the [Feature](feature-table.md) and [FeatureComponents](featurecomponents-table.md) tables for features with 1600 or more components.</span></span>

## <a name="result"></a><span data-ttu-id="6b7c8-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="6b7c8-105">Result</span></span>

<span data-ttu-id="6b7c8-106">ICE47 envía un mensaje de error si una característica supera el límite máximo de 1600 componentes por característica.</span><span class="sxs-lookup"><span data-stu-id="6b7c8-106">ICE47 posts an error message if a feature exceeds the maximum limit of 1600 components per feature.</span></span>

## <a name="example"></a><span data-ttu-id="6b7c8-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b7c8-107">Example</span></span>

<span data-ttu-id="6b7c8-108">ICE47 notificaría la siguiente ADVERTENCIA:</span><span class="sxs-lookup"><span data-stu-id="6b7c8-108">ICE47 would report the following warning:</span></span>

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

<span data-ttu-id="6b7c8-109">[Tabla de características](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6b7c8-109">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="6b7c8-110">Característica</span><span class="sxs-lookup"><span data-stu-id="6b7c8-110">Feature</span></span>  |
|----------|
| <span data-ttu-id="6b7c8-111">Feature1</span><span class="sxs-lookup"><span data-stu-id="6b7c8-111">Feature1</span></span> |



 

<span data-ttu-id="6b7c8-112">[Tabla FeatureComponents](featurecomponents-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="6b7c8-112">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="6b7c8-113">Acción</span><span class="sxs-lookup"><span data-stu-id="6b7c8-113">Action</span></span>   | <span data-ttu-id="6b7c8-114">Condición</span><span class="sxs-lookup"><span data-stu-id="6b7c8-114">Condition</span></span>     |
|----------|---------------|
| <span data-ttu-id="6b7c8-115">Feature1</span><span class="sxs-lookup"><span data-stu-id="6b7c8-115">Feature1</span></span> | <span data-ttu-id="6b7c8-116">Component1</span><span class="sxs-lookup"><span data-stu-id="6b7c8-116">Component1</span></span>    |
| <span data-ttu-id="6b7c8-117">Feature1</span><span class="sxs-lookup"><span data-stu-id="6b7c8-117">Feature1</span></span> | <span data-ttu-id="6b7c8-118">Component1600</span><span class="sxs-lookup"><span data-stu-id="6b7c8-118">Component1600</span></span> |



 

<span data-ttu-id="6b7c8-119">Para corregir esta advertencia, intente dividir la característica en varias características.</span><span class="sxs-lookup"><span data-stu-id="6b7c8-119">To fix this warning, try splitting the feature into several features</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b7c8-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b7c8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b7c8-121">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="6b7c8-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



