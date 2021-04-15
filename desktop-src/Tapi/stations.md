---
description: Los conjuntos de estaciones que se supervisan a través de un vínculo de terceros se modelan como un dispositivo de línea y, posiblemente, un dispositivo telefónico asociado.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688620"
---
# <a name="stations"></a><span data-ttu-id="20538-103">Cadenas</span><span class="sxs-lookup"><span data-stu-id="20538-103">Stations</span></span>

<span data-ttu-id="20538-104">Los conjuntos de estaciones que se supervisan a través de un vínculo de terceros se modelan como un dispositivo de línea y, posiblemente, un dispositivo telefónico asociado.</span><span class="sxs-lookup"><span data-stu-id="20538-104">Station sets being monitored through a third-party link are modeled as a line device and possibly an associated phone device.</span></span> <span data-ttu-id="20538-105">El dispositivo de línea puede tener varias direcciones, si el terminal modelado admite más de un número de directorio (DN).</span><span class="sxs-lookup"><span data-stu-id="20538-105">The line device can have multiple addresses, if the modeled terminal supports more than one directory number (DN).</span></span> <span data-ttu-id="20538-106">Varios aspectos de la llamada en el mismo DN se pueden modelar como una sola dirección que admite varias llamadas.</span><span class="sxs-lookup"><span data-stu-id="20538-106">Multiple call appearances on the same DN can be modeled as a single address that supports multiple calls.</span></span>

<span data-ttu-id="20538-107">Las llamadas entre dos estaciones del conmutador tienen dos identificadores de llamada: uno que asigna la vista de llamada de la primera estación (en su dispositivo de línea) y el otro, que proporcionan la vista de llamada de la segunda estación (en su dispositivo de línea).</span><span class="sxs-lookup"><span data-stu-id="20538-107">Calls between two stations on the switch have two call handles, one giving the call view from the first station (on its line device), and the other giving the call view from the second station (on its line device).</span></span> <span data-ttu-id="20538-108">Por ejemplo, una [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) de terceros colocada por una aplicación en el servidor se dirigirá al dispositivo de línea asociado a la estación desde la que se va a marcar la llamada; en esa línea se crearía un identificador de llamada, en la dirección especificada en [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (con lo que se proporciona el control sobre qué DN se usa en un teléfono que admite varios DNS).</span><span class="sxs-lookup"><span data-stu-id="20538-108">For example, a third-party [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) placed by an application on the server would be directed to the line device associated with the station from which the call is to be dialed; a call handle would be created on that line, on the address specified in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (thereby giving control over which DN is used on a phone that supports multiple DNs).</span></span> <span data-ttu-id="20538-109">Cuando se ofrece la llamada a la dirección de destino, se crea un nuevo identificador de llamada que muestra una llamada en el estado de la *oferta* . las aplicaciones sabrán que era otra vista de la misma llamada por el miembro **dwCallID** de [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) que es igual para ambas llamadas.</span><span class="sxs-lookup"><span data-stu-id="20538-109">When the call is offered to the destination address, a new call handle showing a call in *offering* state is created; applications would know that it was another view of the same call by the **dwCallID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) being equal for both calls.</span></span> <span data-ttu-id="20538-110">Ambas llamadas pasarán a *estar inactivas* cuando se quitó la llamada; una llamada podría quitarse de la aplicación de terceros mediante una [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) en cualquiera de los identificadores de llamada.</span><span class="sxs-lookup"><span data-stu-id="20538-110">Both calls would go *idle* when the call was dropped; a call could be dropped from the third-party application by doing a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on either of the call handles.</span></span>

 

 



