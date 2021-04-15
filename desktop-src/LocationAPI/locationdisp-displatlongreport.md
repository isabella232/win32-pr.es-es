---
description: Representa un informe de latitud y longitud.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: Objeto LocationDisp. DispLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688640"
---
# <a name="locationdispdisplatlongreport-object"></a><span data-ttu-id="c321d-103">Objeto LocationDisp. DispLatLongReport</span><span class="sxs-lookup"><span data-stu-id="c321d-103">LocationDisp.DispLatLongReport object</span></span>

<span data-ttu-id="c321d-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="c321d-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c321d-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="c321d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c321d-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c321d-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="c321d-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="c321d-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="c321d-108">Representa un informe de latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="c321d-108">Represents a latitude/longitude report.</span></span>

## <a name="members"></a><span data-ttu-id="c321d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c321d-109">Members</span></span>

<span data-ttu-id="c321d-110">El objeto **LocationDisp. DispLatLongReport** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c321d-110">The **LocationDisp.DispLatLongReport** object has these types of members:</span></span>

-   [<span data-ttu-id="c321d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c321d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c321d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c321d-112">Properties</span></span>

<span data-ttu-id="c321d-113">El objeto **LocationDisp. DispLatLongReport** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c321d-113">The **LocationDisp.DispLatLongReport** object has these properties.</span></span>



| <span data-ttu-id="c321d-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c321d-114">Property</span></span>                                                                         | <span data-ttu-id="c321d-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="c321d-115">Access type</span></span>          | <span data-ttu-id="c321d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="c321d-116">Description</span></span>                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c321d-117">**Altitud**</span><span class="sxs-lookup"><span data-stu-id="c321d-117">**Altitude**</span></span>](locationdisp-displatlongreport-altitude.md)<br/>           | <span data-ttu-id="c321d-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c321d-118">Read-only</span></span><br/> | <span data-ttu-id="c321d-119">Altitud actual, en metros.</span><span class="sxs-lookup"><span data-stu-id="c321d-119">Current altitude, in meters.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="c321d-120">**AltitudeError**</span><span class="sxs-lookup"><span data-stu-id="c321d-120">**AltitudeError**</span></span>](locationdisp-displatlongreport-altitudeerror.md)<br/> | <span data-ttu-id="c321d-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c321d-121">Read-only</span></span><br/> | <span data-ttu-id="c321d-122">Error de altitud, en metros.</span><span class="sxs-lookup"><span data-stu-id="c321d-122">Altitude error, in meters.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="c321d-123">**ErrorRadius**</span><span class="sxs-lookup"><span data-stu-id="c321d-123">**ErrorRadius**</span></span>](locationdisp-displatlongreport-errorradius.md)<br/>     | <span data-ttu-id="c321d-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c321d-124">Read-only</span></span><br/> | <span data-ttu-id="c321d-125">Distancia desde la ubicación indicada, en metros.</span><span class="sxs-lookup"><span data-stu-id="c321d-125">A distance from the reported location, in meters.</span></span> <span data-ttu-id="c321d-126">Combinado con la ubicación indicada como origen, este radio describe el círculo en el que se encuentra la ubicación real Proably.</span><span class="sxs-lookup"><span data-stu-id="c321d-126">Combined with the reported location as the origin, this radius describes the circle in which the actual location is proably located.</span></span><br/> |
| [<span data-ttu-id="c321d-127">**Latitud**</span><span class="sxs-lookup"><span data-stu-id="c321d-127">**Latitude**</span></span>](locationdisp-displatlongreport-latitude.md)<br/>           | <span data-ttu-id="c321d-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c321d-128">Read-only</span></span><br/> | <span data-ttu-id="c321d-129">Latitud actual, en grados.</span><span class="sxs-lookup"><span data-stu-id="c321d-129">Current latitude, in degrees.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="c321d-130">**Longitud**</span><span class="sxs-lookup"><span data-stu-id="c321d-130">**Longitude**</span></span>](locationdisp-displatlongreport-longitude.md)<br/>         | <span data-ttu-id="c321d-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c321d-131">Read-only</span></span><br/> | <span data-ttu-id="c321d-132">Longitud actual, en grados.</span><span class="sxs-lookup"><span data-stu-id="c321d-132">Current longitude, in degrees.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="c321d-133">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="c321d-133">**Timestamp**</span></span>](locationdisp-displatlongreport-timestamp.md)<br/>         | <span data-ttu-id="c321d-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c321d-134">Read-only</span></span><br/> | <span data-ttu-id="c321d-135">Fecha y hora en que se generó el informe.</span><span class="sxs-lookup"><span data-stu-id="c321d-135">The date and time when the report was generated.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c321d-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c321d-136">Remarks</span></span>

<span data-ttu-id="c321d-137">Puede recuperar este objeto a través de la propiedad [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) del objeto [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="c321d-137">You can retrieve this object through the [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) property of the [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) object.</span></span> <span data-ttu-id="c321d-138">Puede recibir este objeto a través del evento [**NewLatLongReport**](newlatlongreport.md) .</span><span class="sxs-lookup"><span data-stu-id="c321d-138">You can receive this object through the [**NewLatLongReport**](newlatlongreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="c321d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c321d-139">Requirements</span></span>



| <span data-ttu-id="c321d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c321d-140">Requirement</span></span> | <span data-ttu-id="c321d-141">Value</span><span class="sxs-lookup"><span data-stu-id="c321d-141">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="c321d-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c321d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c321d-143">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c321d-143">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c321d-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c321d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c321d-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c321d-145">None supported</span></span><br/>                  |



 

