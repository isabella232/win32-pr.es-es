---
title: Traducción de coordenadas de eventos
description: Traducción de coordenadas de eventos
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778756"
---
# <a name="event-coordinate-translation"></a><span data-ttu-id="7c222-103">Traducción de coordenadas de eventos</span><span class="sxs-lookup"><span data-stu-id="7c222-103">Event Coordinate Translation</span></span>

<span data-ttu-id="7c222-104">La especificación 96 para los controles requiere que las coordenadas pasadas para los eventos desencadenados por el control cambien de HIMETRIC a puntos basados en.</span><span class="sxs-lookup"><span data-stu-id="7c222-104">The 96 specification for controls requires that coordinates passed for events fired by the control change from being HIMETRIC to being points based.</span></span> <span data-ttu-id="7c222-105">Este cambio hace que el evento pase de coordenadas en línea con propiedades y métodos, por lo que la conversión de coordenadas ya no es responsabilidad del contenedor.</span><span class="sxs-lookup"><span data-stu-id="7c222-105">This change brings the event passing of coordinates in line with properties and methods and thus coordinate translation is no longer the responsibility of the container.</span></span> <span data-ttu-id="7c222-106">Esto produce ciertos problemas de compatibilidad en los que un control desencadena eventos mediante una base de coordenadas que no espera, solo debe ser un problema en el que un contenedor de control de 96 hospeda un control anterior a 96 anterior como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="7c222-106">This raises certain compatibility issues where a control fires events using a coordinate base that it is not expecting, this should only be an issue where a 96 control container is hosting an older pre-96 control as follows:</span></span>

-   <span data-ttu-id="7c222-107">Cuando un contenedor anterior a 96 hospeda un control 96, el control presentará las coordenadas de eventos como puntos, por lo que el contenedor no tendrá ningún problema porque el contenedor debe reconocer el tipo de parámetro.</span><span class="sxs-lookup"><span data-stu-id="7c222-107">When an older pre-96 container hosts a 96 control the control will present the event coordinates as points, this should not cause the container any problems as the container should recognize the parameter type.</span></span>
-   <span data-ttu-id="7c222-108">Cuando un contenedor 96 hospeda un control anterior a 96, el control presentará el contenedor con coordenadas y esperará el contenedor a cualquier traducción necesaria.</span><span class="sxs-lookup"><span data-stu-id="7c222-108">When a 96 container hosts a pre-96 control the control will present the container with coordinates and expect the container to any translation necessary.</span></span> <span data-ttu-id="7c222-109">Sin embargo, el contenedor 96 esperará que un control se ajuste a la especificación de los controles 96 y presente sus coordenadas como puntos.</span><span class="sxs-lookup"><span data-stu-id="7c222-109">However the 96 container will be expecting a control to conform to the 96 controls specification and present its coordinates as points.</span></span> <span data-ttu-id="7c222-110">El control usa el método [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) en la interfaz [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) proporcionada por el contenedor de la misma manera que para las propiedades y los métodos para lograrlo.</span><span class="sxs-lookup"><span data-stu-id="7c222-110">The control uses the [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) method on the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface provided by the container in the same way as it does for properties and methods to achieve this.</span></span>

<span data-ttu-id="7c222-111">Como resultado, el usuario de un contenedor 96 que hospede controles anteriores a 96 tendrá que tener en cuenta que puede ser necesaria una traducción adicional de las coordenadas cuando se activan los eventos.</span><span class="sxs-lookup"><span data-stu-id="7c222-111">As a result the user of a 96 container hosting pre-96 controls will need to be aware that further translation of coordinates may be necessary when events are fired.</span></span>

 

 




