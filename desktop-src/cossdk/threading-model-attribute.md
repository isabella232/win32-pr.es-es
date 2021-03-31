---
description: COM+ administra los subprocesos. Cada componente COM tiene una propiedad ThreadingModel que se puede especificar al desarrollar el componente. Esta propiedad determina cómo se asignan los objetos de componentes a los subprocesos para la ejecución del método.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Atributo del modelo de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423267"
---
# <a name="threading-model-attribute"></a><span data-ttu-id="d270d-105">Atributo del modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="d270d-105">Threading Model Attribute</span></span>

<span data-ttu-id="d270d-106">COM+ administra los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d270d-106">COM+ manages threads for you.</span></span> <span data-ttu-id="d270d-107">Cada componente COM tiene una propiedad **ThreadingModel** que se puede especificar al desarrollar el componente.</span><span class="sxs-lookup"><span data-stu-id="d270d-107">Every COM component has a **ThreadingModel** property that you can specify when you develop the component.</span></span> <span data-ttu-id="d270d-108">Esta propiedad determina cómo se asignan los objetos del componente a los subprocesos para la ejecución del método.</span><span class="sxs-lookup"><span data-stu-id="d270d-108">This property determines how the component's objects are assigned to threads for method execution.</span></span>

<span data-ttu-id="d270d-109">Puede usar la herramienta administrativa Servicios de componentes para ver la propiedad modelo de subprocesos; para ello, haga clic con el botón secundario en un componente de la carpeta **componentes** , haga clic en **propiedades** y, a continuación, haga clic en la pestaña **simultaneidad** . En el **modelo de subprocesos**, los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d270d-109">You can use the Component Services administrative tool to view the threading-model property by right-clicking a component in the **Components** folder, clicking **Properties**, and then clicking the **Concurrency** tab. Under **Threading Model**, the possible values are as follows:</span></span>

-   <span data-ttu-id="d270d-110">**Apartamento de subproceso principal**</span><span class="sxs-lookup"><span data-stu-id="d270d-110">**Main Thread Apartment**</span></span>
-   <span data-ttu-id="d270d-111">**Apartamento de un solo subproceso**</span><span class="sxs-lookup"><span data-stu-id="d270d-111">**Single Thread Apartment**</span></span>
-   <span data-ttu-id="d270d-112">**Apartamento de subprocesos libre**</span><span class="sxs-lookup"><span data-stu-id="d270d-112">**Free Thread Apartment**</span></span>
-   <span data-ttu-id="d270d-113">**Apartamento neutro**</span><span class="sxs-lookup"><span data-stu-id="d270d-113">**Neutral Apartment**</span></span>
-   <span data-ttu-id="d270d-114">**Cualquier apartamento**</span><span class="sxs-lookup"><span data-stu-id="d270d-114">**Any Apartment**</span></span>

<span data-ttu-id="d270d-115">El modelo de subprocesos preferido para COM+ es el [Apartamento neutro](neutral-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="d270d-115">The preferred threading model for COM+ is the [neutral apartment](neutral-apartments.md).</span></span> <span data-ttu-id="d270d-116">Sin embargo, si no se especifica un modelo de subprocesos para el componente, COM+ utiliza el apartamento de subproceso principal, que es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d270d-116">However, if you do not specify a threading model for your component, COM+ uses the main thread apartment, which is the default.</span></span>

> [!Note]  
> <span data-ttu-id="d270d-117">Para obtener información más detallada, vea [elegir el modelo de subprocesos](/windows/desktop/com/choosing-the-threading-model).</span><span class="sxs-lookup"><span data-stu-id="d270d-117">For more detailed information, see [Choosing the Threading Model](/windows/desktop/com/choosing-the-threading-model).</span></span>

 

<span data-ttu-id="d270d-118">En la tabla siguiente se muestra el modelo de programación para apartamentos en COM+.</span><span class="sxs-lookup"><span data-stu-id="d270d-118">The following table shows the programming model for apartments in COM+.</span></span>



| <span data-ttu-id="d270d-119">Modelo</span><span class="sxs-lookup"><span data-stu-id="d270d-119">Model</span></span>                     | <span data-ttu-id="d270d-120">Procesamiento</span><span class="sxs-lookup"><span data-stu-id="d270d-120">Apartment</span></span>                                                 | <span data-ttu-id="d270d-121">Gratuito</span><span class="sxs-lookup"><span data-stu-id="d270d-121">Free</span></span>                               | <span data-ttu-id="d270d-122">Ambos</span><span class="sxs-lookup"><span data-stu-id="d270d-122">Both</span></span>                               | <span data-ttu-id="d270d-123">Neutra</span><span class="sxs-lookup"><span data-stu-id="d270d-123">Neutral</span></span>                      | <span data-ttu-id="d270d-124">No especificado</span><span class="sxs-lookup"><span data-stu-id="d270d-124">Not Specified</span></span>                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| <span data-ttu-id="d270d-125">Subproceso único, no principal</span><span class="sxs-lookup"><span data-stu-id="d270d-125">Single-threaded, not main</span></span> | <span data-ttu-id="d270d-126">Creado en el apartamento actual</span><span class="sxs-lookup"><span data-stu-id="d270d-126">Created in current apartment</span></span>                              | <span data-ttu-id="d270d-127">Creado en Apartamento multiproceso</span><span class="sxs-lookup"><span data-stu-id="d270d-127">Created in multithreaded apartment</span></span> | <span data-ttu-id="d270d-128">Creado en el apartamento actual</span><span class="sxs-lookup"><span data-stu-id="d270d-128">Created in current apartment</span></span>       | <span data-ttu-id="d270d-129">Creado en Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="d270d-129">Created in neutral apartment</span></span> | <span data-ttu-id="d270d-130">Creado en el contenedor principal de subprocesos</span><span class="sxs-lookup"><span data-stu-id="d270d-130">Created in main threaded apartment</span></span> |
| <span data-ttu-id="d270d-131">Subproceso único, principal</span><span class="sxs-lookup"><span data-stu-id="d270d-131">Single-threaded, main</span></span>     | <span data-ttu-id="d270d-132">Creado en el apartamento actual</span><span class="sxs-lookup"><span data-stu-id="d270d-132">Created in current apartment</span></span>                              | <span data-ttu-id="d270d-133">Creado en Apartamento multiproceso</span><span class="sxs-lookup"><span data-stu-id="d270d-133">Created in multithreaded apartment</span></span> | <span data-ttu-id="d270d-134">Creado en el apartamento actual</span><span class="sxs-lookup"><span data-stu-id="d270d-134">Created in current apartment</span></span>       | <span data-ttu-id="d270d-135">Creado en Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="d270d-135">Created in neutral apartment</span></span> | <span data-ttu-id="d270d-136">Creado en el apartamento actual</span><span class="sxs-lookup"><span data-stu-id="d270d-136">Created in current apartment</span></span>       |
| <span data-ttu-id="d270d-137">Multiproceso</span><span class="sxs-lookup"><span data-stu-id="d270d-137">Multithreaded</span></span>             | <span data-ttu-id="d270d-138">Creado en un contenedor uniproceso de host</span><span class="sxs-lookup"><span data-stu-id="d270d-138">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="d270d-139">Creado en Apartamento multiproceso</span><span class="sxs-lookup"><span data-stu-id="d270d-139">Created in multithreaded apartment</span></span> | <span data-ttu-id="d270d-140">Creado en Apartamento multiproceso</span><span class="sxs-lookup"><span data-stu-id="d270d-140">Created in multithreaded apartment</span></span> | <span data-ttu-id="d270d-141">Creado en Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="d270d-141">Created in neutral apartment</span></span> | <span data-ttu-id="d270d-142">Creado en el contenedor principal de subprocesos</span><span class="sxs-lookup"><span data-stu-id="d270d-142">Created in main threaded apartment</span></span> |
| <span data-ttu-id="d270d-143">Neutro (en el subproceso STA)</span><span class="sxs-lookup"><span data-stu-id="d270d-143">Neutral (on STA thread)</span></span>   | <span data-ttu-id="d270d-144">Creado en un contenedor uniproceso de host para este subproceso</span><span class="sxs-lookup"><span data-stu-id="d270d-144">Created in host single-threaded apartment for this thread</span></span> | <span data-ttu-id="d270d-145">Creado en Apartamento multiproceso</span><span class="sxs-lookup"><span data-stu-id="d270d-145">Created in multithreaded apartment</span></span> | <span data-ttu-id="d270d-146">Creado en Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="d270d-146">Created in neutral apartment</span></span>       | <span data-ttu-id="d270d-147">Creado en Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="d270d-147">Created in neutral apartment</span></span> | <span data-ttu-id="d270d-148">Creado en el contenedor principal de subprocesos</span><span class="sxs-lookup"><span data-stu-id="d270d-148">Created in main threaded apartment</span></span> |
| <span data-ttu-id="d270d-149">Neutro (en subproceso MTA)</span><span class="sxs-lookup"><span data-stu-id="d270d-149">Neutral (on MTA thread)</span></span>   | <span data-ttu-id="d270d-150">Creado en un contenedor uniproceso de host</span><span class="sxs-lookup"><span data-stu-id="d270d-150">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="d270d-151">Creado en Apartamento multiproceso</span><span class="sxs-lookup"><span data-stu-id="d270d-151">Created in multithreaded apartment</span></span> | <span data-ttu-id="d270d-152">Creado en Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="d270d-152">Created in neutral apartment</span></span>       | <span data-ttu-id="d270d-153">Creado en Apartamento neutro</span><span class="sxs-lookup"><span data-stu-id="d270d-153">Created in neutral apartment</span></span> | <span data-ttu-id="d270d-154">Creado en el contenedor principal de subprocesos</span><span class="sxs-lookup"><span data-stu-id="d270d-154">Created in main threaded apartment</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d270d-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d270d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d270d-156">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="d270d-156">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
