---
description: La API de sensor puede proporcionar notificaciones de eventos.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Acerca de los eventos de la API de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912238"
---
# <a name="about-sensor-api-events"></a><span data-ttu-id="9dafe-103">Acerca de los eventos de la API de sensor</span><span class="sxs-lookup"><span data-stu-id="9dafe-103">About Sensor API Events</span></span>

<span data-ttu-id="9dafe-104">La API de sensor puede proporcionar notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="9dafe-104">The Sensor API can provide event notifications.</span></span>

<span data-ttu-id="9dafe-105">Al registrarse para recibir eventos, a través de [**ISensor:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) o [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), debe proporcionar un puntero a una interfaz de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="9dafe-105">When you register to receive events, through either [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) or [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), you must provide a pointer to a callback interface.</span></span> <span data-ttu-id="9dafe-106">Debe implementar los métodos de la interfaz de devolución de llamada en el código.</span><span class="sxs-lookup"><span data-stu-id="9dafe-106">You must implement the methods of the callback interface in your code.</span></span> <span data-ttu-id="9dafe-107">La API de sensor define las siguientes interfaces de devolución de llamada:</span><span class="sxs-lookup"><span data-stu-id="9dafe-107">The Sensor API defines the following callback interfaces:</span></span>

-   <span data-ttu-id="9dafe-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="9dafe-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="9dafe-109">Implemente esta interfaz para recibir eventos de los sensores.</span><span class="sxs-lookup"><span data-stu-id="9dafe-109">Implement this interface to receive events from sensors.</span></span> <span data-ttu-id="9dafe-110">Los sensores pueden notificar a la aplicación los nuevos datos, los cambios en el estado del sensor, la desconexión del sensor y los eventos personalizados definidos por el fabricante del sensor.</span><span class="sxs-lookup"><span data-stu-id="9dafe-110">Sensors can notify your application about new data, changes in sensor state, sensor disconnection, and custom events defined by the sensor manufacturer.</span></span>
-   <span data-ttu-id="9dafe-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="9dafe-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span> <span data-ttu-id="9dafe-112">Implemente esta interfaz para recibir eventos del administrador del sensor.</span><span class="sxs-lookup"><span data-stu-id="9dafe-112">Implement this interface to receive events from the sensor manager.</span></span> <span data-ttu-id="9dafe-113">El administrador del sensor puede notificar a la aplicación cuando se conecta un sensor y, por tanto, puede estar disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="9dafe-113">The sensor manager can notify your application when a sensor connects, and therefore may be available for use.</span></span>

<span data-ttu-id="9dafe-114">Puede cancelar las notificaciones de eventos llamando a [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) de nuevo, esta vez pasando un valor **null** a través del parámetro.</span><span class="sxs-lookup"><span data-stu-id="9dafe-114">You can cancel event notifications by calling [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) again, this time passing a **NULL** value through the parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dafe-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9dafe-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dafe-116">Uso de eventos de la API de sensor</span><span class="sxs-lookup"><span data-stu-id="9dafe-116">Using Sensor API Events</span></span>](using-sensor-api-events.md)
</dt> </dl>

 

 
