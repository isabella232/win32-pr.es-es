---
title: Cómo funcionan las propiedades
description: Cómo funcionan las propiedades
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Complementos de Media Player de Windows, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- Complementos de procesamiento de señal digital, eco de propiedades de ejemplo
- Complementos DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777100"
---
# <a name="how-properties-work"></a><span data-ttu-id="414e3-108">Cómo funcionan las propiedades</span><span class="sxs-lookup"><span data-stu-id="414e3-108">How Properties Work</span></span>

<span data-ttu-id="414e3-109">Los valores de propiedad se almacenan en variables de miembro.</span><span class="sxs-lookup"><span data-stu-id="414e3-109">Property values are stored in member variables.</span></span>

<span data-ttu-id="414e3-110">Las propiedades se hacen accesibles mediante pares de métodos.</span><span class="sxs-lookup"><span data-stu-id="414e3-110">Properties are made accessible by method pairs.</span></span> <span data-ttu-id="414e3-111">Un método proporciona la implementación para especificar el valor de la propiedad; su nombre comienza por Put \_ .</span><span class="sxs-lookup"><span data-stu-id="414e3-111">One method provides the implementation to specify the property value; its name starts with put\_.</span></span> <span data-ttu-id="414e3-112">El otro método proporciona la implementación para recuperar el valor de la propiedad; su nombre comienza con get \_ .</span><span class="sxs-lookup"><span data-stu-id="414e3-112">The other method provides the implementation to retrieve the property value; its name starts with get\_.</span></span> <span data-ttu-id="414e3-113">La definición de la interfaz está en echo. idl.</span><span class="sxs-lookup"><span data-stu-id="414e3-113">The interface definition is in Echo.idl.</span></span> <span data-ttu-id="414e3-114">Los prototipos de método de propiedad están en echo. h.</span><span class="sxs-lookup"><span data-stu-id="414e3-114">The property method prototypes are in Echo.h.</span></span> <span data-ttu-id="414e3-115">Se implementan en echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="414e3-115">They are implemented in Echo.cpp.</span></span>

<span data-ttu-id="414e3-116">En las tres secciones siguientes se muestra cómo modificar los métodos de propiedad existentes para adaptarlos a sus necesidades y cómo agregar los métodos para una propiedad adicional.</span><span class="sxs-lookup"><span data-stu-id="414e3-116">The next three sections will show you how to modify the existing property methods to suit your needs and how to add the methods for an additional property.</span></span>

-   [<span data-ttu-id="414e3-117">Variables para almacenar propiedades</span><span class="sxs-lookup"><span data-stu-id="414e3-117">Variables to Store Properties</span></span>](variables-to-store-properties.md)
-   [<span data-ttu-id="414e3-118">Modificar la propiedad Scale</span><span class="sxs-lookup"><span data-stu-id="414e3-118">Modifying the Scale Property</span></span>](modifying-the-scale-property.md)
-   [<span data-ttu-id="414e3-119">Agregar la propiedad de combinación húmeda</span><span class="sxs-lookup"><span data-stu-id="414e3-119">Adding the Wet Mix Property</span></span>](adding-the-wet-mix-property.md)

## <a name="related-topics"></a><span data-ttu-id="414e3-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="414e3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="414e3-121">**Eco de propiedades de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="414e3-121">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




