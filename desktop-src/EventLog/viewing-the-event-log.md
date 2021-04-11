---
description: Cuando el usuario inicia Visor de eventos para ver las entradas del registro de eventos, llama a la función ReadEventLog para obtener las estructuras EVENTLOGRECORD.
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: Ver el registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276375"
---
# <a name="viewing-the-event-log"></a><span data-ttu-id="b9a23-103">Ver el registro de eventos</span><span class="sxs-lookup"><span data-stu-id="b9a23-103">Viewing the Event Log</span></span>

<span data-ttu-id="b9a23-104">Cuando el usuario inicia Visor de eventos para ver las entradas del registro de eventos, llama a la función [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) para obtener las estructuras [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="b9a23-104">When the user starts Event Viewer to view the event log entries, it calls the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to obtain the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structures.</span></span> <span data-ttu-id="b9a23-105">El Visor de eventos usa el origen del evento y el identificador de evento para obtener el texto del mensaje para cada evento del archivo de mensaje registrado (indicado por el valor del registro **EventMessageFile** para el origen).</span><span class="sxs-lookup"><span data-stu-id="b9a23-105">The Event Viewer uses the event source and event identifier to get message text for each event from the registered message file (indicated by the **EventMessageFile** registry value for the source).</span></span> <span data-ttu-id="b9a23-106">El Visor de eventos utiliza la función [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) para cargar el archivo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9a23-106">The Event Viewer uses the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message file.</span></span> <span data-ttu-id="b9a23-107">A continuación, el Visor de eventos utiliza la función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) para recuperar la cadena de Descripción base del módulo cargado.</span><span class="sxs-lookup"><span data-stu-id="b9a23-107">The Event Viewer then uses the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function to retrieve the base description string from the loaded module.</span></span> <span data-ttu-id="b9a23-108">Por último, el Visor de eventos reemplaza los parámetros de inserción en la cadena de Descripción base para producir la cadena de mensaje final.</span><span class="sxs-lookup"><span data-stu-id="b9a23-108">Finally, the Event Viewer replaces the insertion parameters in the base description string to yield the final message string.</span></span>

 

 
