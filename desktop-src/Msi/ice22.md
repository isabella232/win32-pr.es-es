---
description: ICE22 usa la tabla FeatureComponents para validar la asignación de características y componentes a los que se hace referencia en la tabla PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667761"
---
# <a name="ice22"></a><span data-ttu-id="b43e4-103">ICE22</span><span class="sxs-lookup"><span data-stu-id="b43e4-103">ICE22</span></span>

<span data-ttu-id="b43e4-104">ICE22 usa la [tabla FeatureComponents](featurecomponents-table.md) para validar la asignación de características y componentes a los que se hace referencia en la [tabla PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="b43e4-104">ICE22 uses the [FeatureComponents table](featurecomponents-table.md) to validate the mapping of features and components referenced in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="b43e4-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="b43e4-105">Result</span></span>

<span data-ttu-id="b43e4-106">ICE22 envía un mensaje de error si las características y los componentes se asignan de forma incorrecta en la [tabla PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="b43e4-106">ICE22 posts an error message if the features and components are mapped incorrectly in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="b43e4-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b43e4-107">Example</span></span>

<span data-ttu-id="b43e4-108">En el ejemplo siguiente, ICE22 envía un error que {00000003-0004-0000-0000-624474732465} no tiene la asignación correcta para las columnas de característica \_ y componente \_ .</span><span class="sxs-lookup"><span data-stu-id="b43e4-108">For the following example ICE22 posts an error that {00000003-0004-0000-0000-624474732465} does not have the correct mapping for the Feature\_ and Component\_ columns.</span></span>

<span data-ttu-id="b43e4-109">[Tabla PublishComponent](publishcomponent-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b43e4-109">[PublishComponent Table](publishcomponent-table.md) (partial)</span></span>



| <span data-ttu-id="b43e4-110">ComponentId</span><span class="sxs-lookup"><span data-stu-id="b43e4-110">ComponentId</span></span>                            | <span data-ttu-id="b43e4-111">Característica\_</span><span class="sxs-lookup"><span data-stu-id="b43e4-111">Feature\_</span></span> | <span data-ttu-id="b43e4-112">Componente\_</span><span class="sxs-lookup"><span data-stu-id="b43e4-112">Component\_</span></span> |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="b43e4-113">Feat1</span><span class="sxs-lookup"><span data-stu-id="b43e4-113">Feat1</span></span>     | <span data-ttu-id="b43e4-114">Comp1</span><span class="sxs-lookup"><span data-stu-id="b43e4-114">Comp1</span></span>       |
| {00000003-0004-0000-0000-624474732465} | <span data-ttu-id="b43e4-115">Feat1</span><span class="sxs-lookup"><span data-stu-id="b43e4-115">Feat1</span></span>     | <span data-ttu-id="b43e4-116">Comp2</span><span class="sxs-lookup"><span data-stu-id="b43e4-116">Comp2</span></span>       |



 

<span data-ttu-id="b43e4-117">[Tabla FeatureComponents](featurecomponents-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="b43e4-117">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="b43e4-118">Característica\_</span><span class="sxs-lookup"><span data-stu-id="b43e4-118">Feature\_</span></span> | <span data-ttu-id="b43e4-119">Componente\_</span><span class="sxs-lookup"><span data-stu-id="b43e4-119">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="b43e4-120">Feat1</span><span class="sxs-lookup"><span data-stu-id="b43e4-120">Feat1</span></span>     | <span data-ttu-id="b43e4-121">Comp1</span><span class="sxs-lookup"><span data-stu-id="b43e4-121">Comp1</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="b43e4-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b43e4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b43e4-123">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="b43e4-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



