---
description: El modelo de objetos de la API de ubicación proporciona los siguientes eventos.
ms.assetid: c7ac0d81-ce36-4991-a0fb-6d3c6cc8efe8
title: Eventos LocationDisp
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55dae79305547bf4e41ee27c727ab9204eb561cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678474"
---
# <a name="locationdisp-events"></a><span data-ttu-id="00735-103">Eventos LocationDisp</span><span class="sxs-lookup"><span data-stu-id="00735-103">LocationDisp Events</span></span>

<span data-ttu-id="00735-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="00735-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00735-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="00735-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="00735-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="00735-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="00735-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="00735-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="00735-108">El modelo de objetos de la API de ubicación proporciona los siguientes eventos.</span><span class="sxs-lookup"><span data-stu-id="00735-108">The Location API object model provides the following events.</span></span>



| <span data-ttu-id="00735-109">Evento</span><span class="sxs-lookup"><span data-stu-id="00735-109">Event</span></span>                                                  | <span data-ttu-id="00735-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="00735-110">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="00735-111">**NewCivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="00735-111">**NewCivicAddressReport**</span></span>](newcivicaddressreport.md) | <span data-ttu-id="00735-112">Se produce cuando se genera un nuevo informe de dirección cívica.</span><span class="sxs-lookup"><span data-stu-id="00735-112">Occurs when a new civic address report is generated.</span></span>      |
| [<span data-ttu-id="00735-113">**NewLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="00735-113">**NewLatLongReport**</span></span>](newlatlongreport.md)           | <span data-ttu-id="00735-114">Se produce cuando se genera un nuevo informe de latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="00735-114">Occurs when a new latitude/longitude report is generated.</span></span> |
| [<span data-ttu-id="00735-115">**StatusChanged**</span><span class="sxs-lookup"><span data-stu-id="00735-115">**StatusChanged**</span></span>](statuschanged.md)                 | <span data-ttu-id="00735-116">Se produce cuando cambia el estado operativo de un informe.</span><span class="sxs-lookup"><span data-stu-id="00735-116">Occurs when the operational status of a report changes.</span></span>   |



 

 

 
