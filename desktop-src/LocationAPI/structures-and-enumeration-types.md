---
description: La API de ubicación define los siguientes tipos de enumeración.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Estructuras y tipos de enumeración (API de ubicación)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678149"
---
# <a name="structures-and-enumeration-types-location-api"></a><span data-ttu-id="cff47-103">Estructuras y tipos de enumeración (API de ubicación)</span><span class="sxs-lookup"><span data-stu-id="cff47-103">Structures and Enumeration Types (Location API)</span></span>

<span data-ttu-id="cff47-104">\[La API de ubicación de Win32 está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="cff47-104">\[The Win32 Location API is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cff47-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="cff47-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="cff47-106">En su lugar, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .</span><span class="sxs-lookup"><span data-stu-id="cff47-106">Instead, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.</span></span> <span data-ttu-id="cff47-107">\]</span><span class="sxs-lookup"><span data-stu-id="cff47-107">\]</span></span>

<span data-ttu-id="cff47-108">La API de ubicación define los siguientes tipos de enumeración.</span><span class="sxs-lookup"><span data-stu-id="cff47-108">The Location API defines the following enumeration types.</span></span>



| <span data-ttu-id="cff47-109">Enumeración</span><span class="sxs-lookup"><span data-stu-id="cff47-109">Enumeration</span></span>                                                                       | <span data-ttu-id="cff47-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cff47-110">Description</span></span>                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="cff47-111">[**\_precisión deseada de la ubicación \_**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cff47-111">[**LOCATION\_DESIRED\_ACCURACY**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span></span>                  | <span data-ttu-id="cff47-112">Define los posibles tipos de precisión deseados.</span><span class="sxs-lookup"><span data-stu-id="cff47-112">Defines the possible desired accuracy types.</span></span>                         |
| [<span data-ttu-id="cff47-113">**\_Estado del informe de ubicación \_**</span><span class="sxs-lookup"><span data-stu-id="cff47-113">**LOCATION\_REPORT\_STATUS**</span></span>](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | <span data-ttu-id="cff47-114">Define el estado posible para los nuevos informes de un tipo de informe determinado.</span><span class="sxs-lookup"><span data-stu-id="cff47-114">Defines possible status for new reports of a particular report type.</span></span> |



 

## <a name="location-constants-from-the-sensor-api"></a><span data-ttu-id="cff47-115">Constantes de ubicación de la API de sensor</span><span class="sxs-lookup"><span data-stu-id="cff47-115">Location Constants from the Sensor API</span></span>

<span data-ttu-id="cff47-116">La API del sensor también define las constantes y las claves de propiedad relacionadas con la ubicación.</span><span class="sxs-lookup"><span data-stu-id="cff47-116">The Sensor API also defines location-related property keys and constants.</span></span> <span data-ttu-id="cff47-117">Las claves de propiedad definidas en Sensors. h se pueden usar para recuperar datos de ubicación de un informe mediante una llamada a [**ILocationReport:: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span><span class="sxs-lookup"><span data-stu-id="cff47-117">The property keys defined in sensors.h can be used to retrieve location data from a report by calling [**ILocationReport::GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span></span>

 

 
