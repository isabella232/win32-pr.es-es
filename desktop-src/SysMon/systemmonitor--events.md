---
title: Eventos SystemMonitor
description: La clase SystemMonitor tiene los siguientes eventos
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665575"
---
# <a name="systemmonitor-events"></a><span data-ttu-id="d6566-103">Eventos SystemMonitor</span><span class="sxs-lookup"><span data-stu-id="d6566-103">SystemMonitor Events</span></span>

<span data-ttu-id="d6566-104">La clase [**SystemMonitor**](systemmonitor.md) tiene los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="d6566-104">The [**SystemMonitor**](systemmonitor.md) class has the following events:</span></span>

-   [<span data-ttu-id="d6566-105">**OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="d6566-105">**OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
-   [<span data-ttu-id="d6566-106">**OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="d6566-106">**OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
-   [<span data-ttu-id="d6566-107">**OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="d6566-107">**OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
-   [<span data-ttu-id="d6566-108">**OnDblClick**</span><span class="sxs-lookup"><span data-stu-id="d6566-108">**OnDblClick**</span></span>](-systemmonitor-ondblclick.md)
-   [<span data-ttu-id="d6566-109">**OnSampleCollected**</span><span class="sxs-lookup"><span data-stu-id="d6566-109">**OnSampleCollected**</span></span>](-systemmonitor-onsamplecollected.md)

> [!Note]  
> <span data-ttu-id="d6566-110">Debe volver del controlador de eventos antes de que expire el [**intervalo de actualización**](systemmonitor-updateinterval.md) ; de lo contrario, SYSMON muestra un cuadro de mensaje que indica al usuario que no pudo muestrear los valores del contador para el intervalo de actualización anterior.</span><span class="sxs-lookup"><span data-stu-id="d6566-110">You must return from the event handler before the [**update interval**](systemmonitor-updateinterval.md) expires; otherwise, SYSMON displays a message box indicating to the user that it was unable to sample counter values for the previous update interval.</span></span>

 

 

 




