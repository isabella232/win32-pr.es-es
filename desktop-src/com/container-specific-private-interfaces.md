---
title: Interfaces privadas de Container-Specific
description: Interfaces privadas de Container-Specific
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357693"
---
# <a name="container-specific-private-interfaces"></a><span data-ttu-id="97bc1-103">Interfaces privadas de Container-Specific</span><span class="sxs-lookup"><span data-stu-id="97bc1-103">Container-Specific Private Interfaces</span></span>

<span data-ttu-id="97bc1-104">Algunos contenedores proporcionan interfaces privadas específicas del contenedor para una funcionalidad adicional o un rendimiento mejorado.</span><span class="sxs-lookup"><span data-stu-id="97bc1-104">Some containers provide container-specific private interfaces for additional functionality or improved performance.</span></span> <span data-ttu-id="97bc1-105">Los controles que dependen de esas interfaces específicas del contenedor deberían, si es posible, trabajar sin esas interfaces específicas del contenedor para que el control funcione en contenedores diferentes.</span><span class="sxs-lookup"><span data-stu-id="97bc1-105">Controls that rely on those container-specific interfaces should, if possible, work without those container-specific interfaces present so that the control functions in different containers.</span></span> <span data-ttu-id="97bc1-106">Por ejemplo, Visual Basic implementa interfaces privadas que proporcionan la funcionalidad de formato de cadena para los controles.</span><span class="sxs-lookup"><span data-stu-id="97bc1-106">For example, Visual Basic implements private interfaces that provide string formatting functionality to controls.</span></span> <span data-ttu-id="97bc1-107">Si un control usa estas interfaces de formato privado, debería poder ejecutarse con compatibilidad de formato predeterminada si estas interfaces no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="97bc1-107">If a control makes use of these private formatting interfaces, it should be able to run with default formatting support if these interfaces are not available.</span></span> <span data-ttu-id="97bc1-108">Si el control puede funcionar sin las interfaces privadas, debe llevar a cabo la acción adecuada (por ejemplo, advertir al usuario de la funcionalidad reducida) pero seguir trabajando.</span><span class="sxs-lookup"><span data-stu-id="97bc1-108">If the control can function without the private interfaces, it should take appropriate action (such as warn the user of reduced functionality) but continue to work.</span></span> <span data-ttu-id="97bc1-109">Si no es una opción, se debe registrar una categoría de componente como sea necesario para que solo los contenedores que admiten esta funcionalidad puedan hospedar estos controles.</span><span class="sxs-lookup"><span data-stu-id="97bc1-109">If this is not an option, a component category should be registered as required so that only containers supporting this functionality can host these controls.</span></span>

 

 




