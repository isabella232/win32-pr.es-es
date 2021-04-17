---
description: ICE41 valida que las entradas de las tablas de clase y extensión hacen referencia a las entradas de la tabla de componentes que implementan el objeto de clase o la extensión del componente.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652814"
---
# <a name="ice41"></a><span data-ttu-id="df3b9-103">ICE41</span><span class="sxs-lookup"><span data-stu-id="df3b9-103">ICE41</span></span>

<span data-ttu-id="df3b9-104">ICE41 valida que las entradas de las tablas de [clase](class-table.md) y [extensión](extension-table.md) hacen referencia a las entradas de la [tabla de componentes](component-table.md) que implementan el objeto de clase o la extensión del componente.</span><span class="sxs-lookup"><span data-stu-id="df3b9-104">ICE41 validates that the entries in the [Class](class-table.md) and [Extension](extension-table.md) tables refer to entries in the [Component table](component-table.md) that implement the class object or extension of the component.</span></span>

## <a name="result"></a><span data-ttu-id="df3b9-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="df3b9-105">Result</span></span>

<span data-ttu-id="df3b9-106">ICE41 publica un error si hay una característica que no contiene el componente que implementa la extensión o el objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="df3b9-106">ICE41 posts an error if there is a feature that does not contain the component implementing the class object or extension.</span></span>

## <a name="example"></a><span data-ttu-id="df3b9-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df3b9-107">Example</span></span>

<span data-ttu-id="df3b9-108">ICE41 notifica los siguientes errores para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="df3b9-108">ICE41 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="df3b9-109">Error ICE41</span><span class="sxs-lookup"><span data-stu-id="df3b9-109">ICE41 error</span></span>                                                                                                                                                                                    | <span data-ttu-id="df3b9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="df3b9-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df3b9-111">{00000000-0000-0000-0000-0000000000000}La clase hace referencia a la característica característica2 y al componente Component1, pero el componente no está asociado a esa característica en la tabla FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="df3b9-111">Class {00000000-0000-0000-0000-0000000000000} references feature Feature2 and component Component1, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span> | <span data-ttu-id="df3b9-112">Hay una característica que no contiene el componente que implementa el objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="df3b9-112">There is a feature that does not contain the component implementing the class object.</span></span> <span data-ttu-id="df3b9-113">Esto significa que el instalador no instala el componente con la característica y que el anuncio puede no funcionar según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="df3b9-113">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="df3b9-114">Para corregir este error, cambie la entrada en la \_ columna característica de la entrada de la [tabla de clases](class-table.md) para que haga referencia a una característica que instala el componente enumerado en la columna componente \_ o cambie la característica y el componente asociados en la [tabla FeatureComponents](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="df3b9-114">To fix this error, change the entry in the Feature\_ column of the [Class table](class-table.md) entry to reference a feature that installs component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/>          |
| <span data-ttu-id="df3b9-115">Extension. Yip hace referencia a la característica Feature1 y al componente Component2, pero el componente no está asociado a esa característica en la tabla FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="df3b9-115">Extension .yip references feature Feature1 and component Component2, but the that Component is not associated with that Feature in the FeatureComponents table.</span></span>                                | <span data-ttu-id="df3b9-116">Hay una característica que no contiene el componente que implementa la extensión.</span><span class="sxs-lookup"><span data-stu-id="df3b9-116">There is a feature that does not contain the component implementing the extension.</span></span> <span data-ttu-id="df3b9-117">Esto significa que el instalador no instala el componente con la característica y que el anuncio puede no funcionar según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="df3b9-117">This means that the installer does not install the component with the feature and that advertising may not work as expected.</span></span> <span data-ttu-id="df3b9-118">Para corregir este error, cambie la entrada en la \_ columna característica de la entrada de la [tabla de extensión](extension-table.md) para que haga referencia a una característica que instala el componente enumerado en la \_ columna componente o cambie la característica y el componente asociados en la [tabla FeatureComponents](featurecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="df3b9-118">To fix this error, change the entry in the Feature\_ column of the [Extension table](extension-table.md) entry to reference a feature that installs the component listed in the Component\_ column or change the feature and component associated in the [FeatureComponents table](featurecomponents-table.md).</span></span><br/> |



 

<span data-ttu-id="df3b9-119">[Tabla FeatureComponents](featurecomponents-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="df3b9-119">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="df3b9-120">Característica\_</span><span class="sxs-lookup"><span data-stu-id="df3b9-120">Feature\_</span></span> |
|-----------|
| <span data-ttu-id="df3b9-121">Feature1</span><span class="sxs-lookup"><span data-stu-id="df3b9-121">Feature1</span></span>  |
| <span data-ttu-id="df3b9-122">Característica2</span><span class="sxs-lookup"><span data-stu-id="df3b9-122">Feature2</span></span>  |



 

<span data-ttu-id="df3b9-123">[Tabla de clases](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="df3b9-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="df3b9-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="df3b9-124">CLSID</span></span>                                  | <span data-ttu-id="df3b9-125">Componente\_</span><span class="sxs-lookup"><span data-stu-id="df3b9-125">Component\_</span></span> | <span data-ttu-id="df3b9-126">Característica\_</span><span class="sxs-lookup"><span data-stu-id="df3b9-126">Feature\_</span></span> |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | <span data-ttu-id="df3b9-127">Component1</span><span class="sxs-lookup"><span data-stu-id="df3b9-127">Component1</span></span>  | <span data-ttu-id="df3b9-128">Característica2</span><span class="sxs-lookup"><span data-stu-id="df3b9-128">Feature2</span></span>  |



 

<span data-ttu-id="df3b9-129">[Tabla de clases](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="df3b9-129">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="df3b9-130">Extensión</span><span class="sxs-lookup"><span data-stu-id="df3b9-130">Extension</span></span> | <span data-ttu-id="df3b9-131">Componente\_</span><span class="sxs-lookup"><span data-stu-id="df3b9-131">Component\_</span></span> | <span data-ttu-id="df3b9-132">Característica\_</span><span class="sxs-lookup"><span data-stu-id="df3b9-132">Feature\_</span></span> |
|-----------|-------------|-----------|
| <span data-ttu-id="df3b9-133">.yip</span><span class="sxs-lookup"><span data-stu-id="df3b9-133">.yip</span></span>      | <span data-ttu-id="df3b9-134">Component2</span><span class="sxs-lookup"><span data-stu-id="df3b9-134">Component2</span></span>  | <span data-ttu-id="df3b9-135">Feature1</span><span class="sxs-lookup"><span data-stu-id="df3b9-135">Feature1</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="df3b9-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df3b9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df3b9-137">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="df3b9-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




