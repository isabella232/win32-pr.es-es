---
description: API de Media Foundation Platform
ms.assetid: 1eb20c44-58cb-4e34-a108-1b3c27d54ff1
title: API de Media Foundation Platform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1e8d8aa0dcd5d7b1184a406e09910a98892f4f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721327"
---
# <a name="media-foundation-platform-apis"></a><span data-ttu-id="8bf9a-103">API de Media Foundation Platform</span><span class="sxs-lookup"><span data-stu-id="8bf9a-103">Media Foundation Platform APIs</span></span>

<span data-ttu-id="8bf9a-104">El nivel de plataforma de Media Foundation contiene primitivos y objetos auxiliares usados por las otras capas.</span><span class="sxs-lookup"><span data-stu-id="8bf9a-104">The platform layer of Media Foundation contains primitives and helper objects used by the other layers.</span></span>

<span data-ttu-id="8bf9a-105">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="8bf9a-105">This section contains the following topics:</span></span>



| <span data-ttu-id="8bf9a-106">Tema</span><span class="sxs-lookup"><span data-stu-id="8bf9a-106">Topic</span></span>                                                                           | <span data-ttu-id="8bf9a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8bf9a-107">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bf9a-108">Inicialización de la plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8bf9a-108">Initializing the Media Foundation Platform</span></span>](initializing-media-foundation.md) | <span data-ttu-id="8bf9a-109">Cómo inicializar la plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8bf9a-109">How to initialize the Media Foundation platform.</span></span>                                                                                                                  |
| [<span data-ttu-id="8bf9a-110">Media Foundation y COM</span><span class="sxs-lookup"><span data-stu-id="8bf9a-110">Media Foundation and COM</span></span>](media-foundation-and-com.md)                        | <span data-ttu-id="8bf9a-111">Describe la interacción entre COM y Microsoft Media Foundation, y define algunos procedimientos recomendados que se deben usar al desarrollar componentes de complemento de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8bf9a-111">Describes the interaction between COM and Microsoft Media Foundation, and defines some best practices to use when developing Media Foundation plug-in components.</span></span> |
| [<span data-ttu-id="8bf9a-112">Métodos de devolución de llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="8bf9a-112">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)              | <span data-ttu-id="8bf9a-113">Cómo llamar a métodos asincrónicos y cómo implementar operaciones asincrónicas en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8bf9a-113">How to call asynchronous methods and how to implement asynchronous operations in Media Foundation.</span></span>                                                                |
| [<span data-ttu-id="8bf9a-114">Colas de trabajo</span><span class="sxs-lookup"><span data-stu-id="8bf9a-114">Work Queues</span></span>](work-queues.md)                                                  | <span data-ttu-id="8bf9a-115">Una cola de trabajo es una manera eficaz de realizar operaciones asincrónicas en otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="8bf9a-115">A work queue is an efficient way to perform asynchronous operations on another thread.</span></span>                                                                            |
| [<span data-ttu-id="8bf9a-116">Generadores de eventos multimedia</span><span class="sxs-lookup"><span data-stu-id="8bf9a-116">Media Event Generators</span></span>](media-event-generators.md)                            | <span data-ttu-id="8bf9a-117">Cómo recibir eventos asincrónicos y cómo generar eventos en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8bf9a-117">How to receive asynchronous events and how to raise events in Media Foundation.</span></span>                                                                                   |
| [<span data-ttu-id="8bf9a-118">Interfaces de servicio</span><span class="sxs-lookup"><span data-stu-id="8bf9a-118">Service Interfaces</span></span>](service-interfaces.md)                                    | <span data-ttu-id="8bf9a-119">Una interfaz de servicio es una interfaz COM que proporciona un objeto, pero que se expone a la aplicación a través de otro objeto.</span><span class="sxs-lookup"><span data-stu-id="8bf9a-119">A service interface is a COM interface provided by one object, but exposed to the application through another object.</span></span>                                             |
| [<span data-ttu-id="8bf9a-120">Objetos de activación</span><span class="sxs-lookup"><span data-stu-id="8bf9a-120">Activation Objects</span></span>](activation-objects.md)                                    | <span data-ttu-id="8bf9a-121">Un objeto de activación es un objeto que crea otro objeto.</span><span class="sxs-lookup"><span data-stu-id="8bf9a-121">An activation object is an object that creates another object.</span></span>                                                                                                    |
| [<span data-ttu-id="8bf9a-122">Reloj de presentación</span><span class="sxs-lookup"><span data-stu-id="8bf9a-122">Presentation Clock</span></span>](presentation-clock.md)                                    | <span data-ttu-id="8bf9a-123">El reloj de la presentación genera la hora de reloj que se usa para controlar la reproducción y también para las secuencias de audio y vídeo sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="8bf9a-123">The presentation clock generates the clock time that is used to control playback, and also to synchronous audio and video streams.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="8bf9a-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bf9a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bf9a-125">Arquitectura de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8bf9a-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="8bf9a-126">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8bf9a-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



