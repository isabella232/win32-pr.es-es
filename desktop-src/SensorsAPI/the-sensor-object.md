---
description: El objeto de sensor representa un sensor determinado.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: El objeto de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667889"
---
# <a name="the-sensor-object"></a><span data-ttu-id="3d18a-103">El objeto de sensor</span><span class="sxs-lookup"><span data-stu-id="3d18a-103">The Sensor Object</span></span>

<span data-ttu-id="3d18a-104">El objeto de sensor representa un sensor determinado.</span><span class="sxs-lookup"><span data-stu-id="3d18a-104">The sensor object represents a particular sensor.</span></span>

<span data-ttu-id="3d18a-105">La API del sensor representa cada sensor como un objeto de sensor.</span><span class="sxs-lookup"><span data-stu-id="3d18a-105">The Sensor API represents each sensor as a sensor object.</span></span> <span data-ttu-id="3d18a-106">Puede trabajar con un objeto de sensor determinado a través de su interfaz [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) .</span><span class="sxs-lookup"><span data-stu-id="3d18a-106">You can work with a particular sensor object through its [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface.</span></span> <span data-ttu-id="3d18a-107">Esta interfaz le permite:</span><span class="sxs-lookup"><span data-stu-id="3d18a-107">This interface enables you to:</span></span>

-   <span data-ttu-id="3d18a-108">Recupere los metadatos sobre el sensor, como su identificador, tipo o nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="3d18a-108">Retrieve metadata about the sensor, such as its ID, type, or friendly name.</span></span>
-   <span data-ttu-id="3d18a-109">Recupera información sobre los datos específicos que el sensor puede proporcionar.</span><span class="sxs-lookup"><span data-stu-id="3d18a-109">Retrieve information about the specific data the sensor can provide.</span></span>
-   <span data-ttu-id="3d18a-110">Recupere los datos de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="3d18a-110">Retrieve the data, synchronously.</span></span>
-   <span data-ttu-id="3d18a-111">Recupera la información de estado, por ejemplo, si el sensor está listo.</span><span class="sxs-lookup"><span data-stu-id="3d18a-111">Retrieve state information, such as whether the sensor is ready.</span></span>
-   <span data-ttu-id="3d18a-112">Especifique los eventos que recibirá el programa.</span><span class="sxs-lookup"><span data-stu-id="3d18a-112">Specify which events your program will receive.</span></span>
-   <span data-ttu-id="3d18a-113">Especifique la interfaz de devolución de llamada que la API de sensor puede usar para proporcionar el programa con notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="3d18a-113">Specify the callback interface that the Sensor API can use to provide your program with event notifications.</span></span>

 

 



