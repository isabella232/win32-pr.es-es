---
description: Información general de la notificación de eventos
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Información general de la notificación de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806074"
---
# <a name="overview-of-event-notification"></a><span data-ttu-id="872e0-103">Información general de la notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="872e0-103">Overview of Event Notification</span></span>

<span data-ttu-id="872e0-104">Un filtro notifica al administrador de gráficos de filtro sobre un evento mediante la publicación de una notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="872e0-104">A filter notifies the Filter Graph Manager about an event by posting an event notification.</span></span> <span data-ttu-id="872e0-105">El evento podría ser algo esperado, como el final de una secuencia, o podría representar un error, como un error al representar un flujo.</span><span class="sxs-lookup"><span data-stu-id="872e0-105">The event could be something expected, such as the end of a stream, or it could represent an error, such as a failure to render a stream.</span></span> <span data-ttu-id="872e0-106">El administrador de gráficos de filtro controla algunos eventos de filtro por sí mismo y deja a otros para que la aplicación los controle.</span><span class="sxs-lookup"><span data-stu-id="872e0-106">The Filter Graph Manager handles some filter events by itself, and it leaves others for the application to handle.</span></span> <span data-ttu-id="872e0-107">Si Filter Graph Manager no controla un evento Filter, coloca la notificación de eventos en una cola.</span><span class="sxs-lookup"><span data-stu-id="872e0-107">If the Filter Graph Manager does not handle a filter event, it places the event notification into a queue.</span></span> <span data-ttu-id="872e0-108">El gráfico de filtros también puede poner en cola sus propias notificaciones de eventos para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="872e0-108">The filter graph can also queue its own event notifications for the application.</span></span>

<span data-ttu-id="872e0-109">Una aplicación recupera los eventos de la cola y los responde en función del tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="872e0-109">An application retrieves events from the queue and responds to them based on the type of event.</span></span> <span data-ttu-id="872e0-110">La notificación de eventos en DirectShow es, por lo tanto, similar al esquema de Message Queue Server de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="872e0-110">Event notification in DirectShow is therefore similar to the Microsoft Windows message queuing scheme.</span></span> <span data-ttu-id="872e0-111">Una aplicación también puede cancelar el comportamiento predeterminado del administrador de gráficos de filtro para un tipo de evento determinado.</span><span class="sxs-lookup"><span data-stu-id="872e0-111">An application can also cancel the Filter Graph Manager's default behavior for a given event type.</span></span> <span data-ttu-id="872e0-112">Después, el administrador de gráficos de filtro coloca esos eventos directamente en la cola para que la aplicación los controle.</span><span class="sxs-lookup"><span data-stu-id="872e0-112">The Filter Graph Manager then puts those events directly into the queue for the application to handle.</span></span>

<span data-ttu-id="872e0-113">Este mecanismo permite</span><span class="sxs-lookup"><span data-stu-id="872e0-113">This mechanism enables</span></span>

-   <span data-ttu-id="872e0-114">El administrador de gráficos de filtro para comunicarse con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="872e0-114">The Filter Graph Manager to communicate with the application.</span></span>
-   <span data-ttu-id="872e0-115">Filtros para comunicarse con la aplicación y el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="872e0-115">Filters to communicate with both the application and the Filter Graph Manager.</span></span>
-   <span data-ttu-id="872e0-116">La aplicación para determinar su grado de implicación en el control de eventos.</span><span class="sxs-lookup"><span data-stu-id="872e0-116">The application to determine its degree of involvement in handling events.</span></span>

 

 



