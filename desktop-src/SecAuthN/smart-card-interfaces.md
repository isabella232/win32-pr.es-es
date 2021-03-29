---
description: Una interfaz de tarjeta inteligente consta de un conjunto predefinido de servicios disponibles dentro de una tarjeta inteligente, los protocolos necesarios para invocar los servicios y cualquier suposición relativa al contexto de los servicios.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Interfaces de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816211"
---
# <a name="smart-card-interfaces"></a><span data-ttu-id="77761-103">Interfaces de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="77761-103">Smart Card Interfaces</span></span>

<span data-ttu-id="77761-104">Una interfaz de [*tarjeta inteligente*](../secgloss/s-gly.md) consta de un conjunto predefinido de servicios disponibles dentro de una *tarjeta inteligente*, los protocolos necesarios para invocar los servicios y cualquier suposición relativa al contexto de los servicios.</span><span class="sxs-lookup"><span data-stu-id="77761-104">A [*smart card*](../secgloss/s-gly.md) interface consists of a predefined set of services available within a *smart card*, the protocols necessary to invoke the services, and any assumptions regarding the context of the services.</span></span>

<span data-ttu-id="77761-105">Con respecto a las tarjetas inteligentes, el término "interfaz" es similar al modo en que se usa en COM, que a su vez es similar en concepto al identificador de la aplicación ISO 7816/5, pero con un ámbito diferente.</span><span class="sxs-lookup"><span data-stu-id="77761-105">With respect to smart cards, the term "interface" is similar to how it is used in COM, which in turn is similar in concept to the ISO 7816/5 application identifier but with a different scope.</span></span>

<span data-ttu-id="77761-106">Cada interfaz de tarjeta inteligente se identifica mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="77761-106">Each smart card interface is identified by a GUID.</span></span> <span data-ttu-id="77761-107">Por ejemplo, se puede definir una interfaz que proporcione información de Bioritmo a su titular.</span><span class="sxs-lookup"><span data-stu-id="77761-107">For example, an interface might be defined that provides biorhythm information to its holder.</span></span> <span data-ttu-id="77761-108">Si una tarjeta inteligente determinada es compatible con este servicio, puede que sea compatible con el GUID de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="77761-108">If a given smart card supports this service, then it may claim to support that interface GUID.</span></span> <span data-ttu-id="77761-109">Mediante el uso de los GUID de interfaz, una aplicación puede buscar un conjunto determinado de interfaces, localizando cualquier tarjeta que admita ese conjunto, para completar una tarea.</span><span class="sxs-lookup"><span data-stu-id="77761-109">Using the interface GUIDs, an application may search for a particular set of interfaces, locating any card that supports that set, to complete a task.</span></span>

<span data-ttu-id="77761-110">Aunque una interfaz tiene un GUID, podría implementarse de forma diferente en distintas tarjetas.</span><span class="sxs-lookup"><span data-stu-id="77761-110">Although an interface has one GUID, it might be implemented differently on different cards.</span></span> <span data-ttu-id="77761-111">Por ejemplo, la interfaz de Bioritmo mencionada anteriormente puede tener varias implementaciones diferentes, pero se hace referencia a todos con el mismo GUID.</span><span class="sxs-lookup"><span data-stu-id="77761-111">For example, the biorhythm interface mentioned above can have several different implementations, yet all are referenced using the same GUID.</span></span> <span data-ttu-id="77761-112">Las distintas implementaciones no cambiarían la interacción entre la aplicación y la tarjeta inteligente. sin embargo, la interacción entre el [*proveedor de servicios*](../secgloss/c-gly.md) y las tarjetas inteligentes puede diferir dependiendo de la implementación de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="77761-112">The different implementations would not change the interaction between the application and the smart card; however, the interaction between the [*service provider*](../secgloss/c-gly.md) and the smart cards may differ depending on the interface's implementation.</span></span>

<span data-ttu-id="77761-113">El conjunto de interfaces que admite una tarjeta inteligente se define durante la introducción de tarjetas inteligentes (consulte [Introducción a las tarjetas inteligentes en el sistema](introducing-smart-cards-to-the-system.md)).</span><span class="sxs-lookup"><span data-stu-id="77761-113">The set of interfaces supported by a smart card is defined during smart card introduction (see [Introducing Smart Cards to the System](introducing-smart-cards-to-the-system.md)).</span></span>

 

 
