---
description: Cada evento puede tener asociados datos específicos del evento.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Datos del evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666704"
---
# <a name="event-data"></a><span data-ttu-id="5389a-103">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="5389a-103">Event Data</span></span>

<span data-ttu-id="5389a-104">Cada evento puede tener asociados datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="5389a-104">Each event can have event-specific data associated with it.</span></span> <span data-ttu-id="5389a-105">El Visor de eventos no interpreta estos datos; solo muestra datos adicionales en formato hexadecimal y de texto combinados.</span><span class="sxs-lookup"><span data-stu-id="5389a-105">The Event Viewer does not interpret this data; it displays extra data only in a combined hexadecimal and text format.</span></span> <span data-ttu-id="5389a-106">El límite máximo del tamaño de un evento en el registro par es 0x3FFFF bytes.</span><span class="sxs-lookup"><span data-stu-id="5389a-106">The maximum limit on the size of an event in the even log is 0x3FFFF bytes.</span></span> <span data-ttu-id="5389a-107">Por lo tanto, use los datos específicos del evento con moderación, incluido solo si está seguro de que será útil para alguien que depure un problema.</span><span class="sxs-lookup"><span data-stu-id="5389a-107">Therefore, use event-specific data sparingly, including it only if you are sure it will be useful to someone debugging a problem.</span></span> <span data-ttu-id="5389a-108">Por ejemplo, muchos eventos relacionados con la red incluyen bloques de control de red (NCB) como datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="5389a-108">For example, many network-related events include network control blocks (NCB) as event-specific data.</span></span>

<span data-ttu-id="5389a-109">Cuando se usan datos específicos del evento, la última parte de la cadena de descripción debe proporcionar una nota sobre la información proporcionada como datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="5389a-109">When you use event-specific data, the last part of its description string should provide a note about the information provided as event-specific data.</span></span> <span data-ttu-id="5389a-110">Por ejemplo, el software de red podría proporcionar una nota como: "(el NCB es los datos de evento)". Como Convención, use paréntesis alrededor de estos comentarios, como se indica en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5389a-110">For example, the network software could provide a note such as: "(The NCB is the event data.)" As a convention, use parentheses around such remarks, as indicated in this example.</span></span>

<span data-ttu-id="5389a-111">También puede utilizar datos específicos del evento para almacenar información que la aplicación puede procesar independientemente del Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="5389a-111">You can also use event-specific data to store information the application can process independently of the Event Viewer.</span></span> <span data-ttu-id="5389a-112">Por ejemplo, puede escribir un visor específicamente para los eventos o escribir un programa que examine el registro y cree un informe que incluya información de los datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="5389a-112">For example, you could write a viewer specifically for your events, or write a program that scans the log and creates a report that includes information from the event-specific data.</span></span>

 

 



