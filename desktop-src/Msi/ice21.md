---
description: ICE21 valida que todos los componentes de la tabla de componentes pertenezcan a una característica. Usa la tabla FeatureComponents para comprobar esta asignación.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667762"
---
# <a name="ice21"></a><span data-ttu-id="4a22a-104">ICE21</span><span class="sxs-lookup"><span data-stu-id="4a22a-104">ICE21</span></span>

<span data-ttu-id="4a22a-105">ICE21 valida que todos los componentes de la [tabla de componentes](component-table.md) pertenezcan a una característica.</span><span class="sxs-lookup"><span data-stu-id="4a22a-105">ICE21 validates that every component in the [Component table](component-table.md) belongs to a feature.</span></span> <span data-ttu-id="4a22a-106">Usa la [tabla FeatureComponents](featurecomponents-table.md) para comprobar esta asignación.</span><span class="sxs-lookup"><span data-stu-id="4a22a-106">It uses the [FeatureComponents table](featurecomponents-table.md) to check for this mapping.</span></span>

## <a name="result"></a><span data-ttu-id="4a22a-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="4a22a-107">Result</span></span>

<span data-ttu-id="4a22a-108">ICE21 envía un mensaje de error si el paquete de instalación contiene un componente que no pertenece a una característica.</span><span class="sxs-lookup"><span data-stu-id="4a22a-108">ICE21 posts an error message if the installation package contains a component that does not belong to a feature.</span></span>

## <a name="example"></a><span data-ttu-id="4a22a-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a22a-109">Example</span></span>

<span data-ttu-id="4a22a-110">En el ejemplo siguiente, ICE21 envía un mensaje de error que indica que el componente Comp1 no se asigna a ninguna característica.</span><span class="sxs-lookup"><span data-stu-id="4a22a-110">For the following example, ICE21 posts an error message stating that the component Comp1 does not map to any feature.</span></span>

<span data-ttu-id="4a22a-111">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="4a22a-111">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="4a22a-112">Componente</span><span class="sxs-lookup"><span data-stu-id="4a22a-112">Component</span></span> |
|-----------|
| <span data-ttu-id="4a22a-113">Comp1</span><span class="sxs-lookup"><span data-stu-id="4a22a-113">Comp1</span></span>     |
| <span data-ttu-id="4a22a-114">Comp2</span><span class="sxs-lookup"><span data-stu-id="4a22a-114">Comp2</span></span>     |



 

<span data-ttu-id="4a22a-115">[Tabla FeatureComponents](featurecomponents-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="4a22a-115">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="4a22a-116">Característica</span><span class="sxs-lookup"><span data-stu-id="4a22a-116">Feature</span></span>  | <span data-ttu-id="4a22a-117">Componente</span><span class="sxs-lookup"><span data-stu-id="4a22a-117">Component</span></span> |
|----------|-----------|
| <span data-ttu-id="4a22a-118">Feature1</span><span class="sxs-lookup"><span data-stu-id="4a22a-118">Feature1</span></span> | <span data-ttu-id="4a22a-119">Comp2</span><span class="sxs-lookup"><span data-stu-id="4a22a-119">Comp2</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="4a22a-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4a22a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a22a-121">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="4a22a-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



