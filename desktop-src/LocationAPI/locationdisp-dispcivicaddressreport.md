---
description: Representa un informe de direcciones cívica.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: Objeto LocationDisp. DispCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a2a96f3d0c2a1fe8e3ac78e5db67ded031a4aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678036"
---
# <a name="locationdispdispcivicaddressreport-object"></a><span data-ttu-id="473a6-103">Objeto LocationDisp. DispCivicAddressReport</span><span class="sxs-lookup"><span data-stu-id="473a6-103">LocationDisp.DispCivicAddressReport object</span></span>

<span data-ttu-id="473a6-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="473a6-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="473a6-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="473a6-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="473a6-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="473a6-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="473a6-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="473a6-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="473a6-108">Representa un informe de direcciones cívica.</span><span class="sxs-lookup"><span data-stu-id="473a6-108">Represents a civic address report.</span></span>

## <a name="members"></a><span data-ttu-id="473a6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="473a6-109">Members</span></span>

<span data-ttu-id="473a6-110">El objeto **LocationDisp. DispCivicAddressReport** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="473a6-110">The **LocationDisp.DispCivicAddressReport** object has these types of members:</span></span>

-   [<span data-ttu-id="473a6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="473a6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="473a6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="473a6-112">Properties</span></span>

<span data-ttu-id="473a6-113">El objeto **LocationDisp. DispCivicAddressReport** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="473a6-113">The **LocationDisp.DispCivicAddressReport** object has these properties.</span></span>



| <span data-ttu-id="473a6-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="473a6-114">Property</span></span>                                                                              | <span data-ttu-id="473a6-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="473a6-115">Access type</span></span>          | <span data-ttu-id="473a6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="473a6-116">Description</span></span>                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [<span data-ttu-id="473a6-117">**AddressLine1**</span><span class="sxs-lookup"><span data-stu-id="473a6-117">**AddressLine1**</span></span>](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | <span data-ttu-id="473a6-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473a6-118">Read-only</span></span><br/> | <span data-ttu-id="473a6-119">La primera línea de una dirección postal.</span><span class="sxs-lookup"><span data-stu-id="473a6-119">The first line of a street address.</span></span><br/>              |
| [<span data-ttu-id="473a6-120">**AddressLine2**</span><span class="sxs-lookup"><span data-stu-id="473a6-120">**AddressLine2**</span></span>](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | <span data-ttu-id="473a6-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473a6-121">Read-only</span></span><br/> | <span data-ttu-id="473a6-122">La segunda línea de una dirección postal.</span><span class="sxs-lookup"><span data-stu-id="473a6-122">The second line of a street address.</span></span><br/>             |
| [<span data-ttu-id="473a6-123">**Ciudad**</span><span class="sxs-lookup"><span data-stu-id="473a6-123">**City**</span></span>](locationdisp-dispcivicaddressreport-city.md)<br/>                   | <span data-ttu-id="473a6-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473a6-124">Read-only</span></span><br/> | <span data-ttu-id="473a6-125">El nombre de la ciudad.</span><span class="sxs-lookup"><span data-stu-id="473a6-125">The city name.</span></span><br/>                                   |
| [<span data-ttu-id="473a6-126">**CountryRegion**</span><span class="sxs-lookup"><span data-stu-id="473a6-126">**CountryRegion**</span></span>](locationdisp-civicaddressreport-countryregion.md)<br/>     | <span data-ttu-id="473a6-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473a6-127">Read-only</span></span><br/> | <span data-ttu-id="473a6-128">Nombre del país o la región.</span><span class="sxs-lookup"><span data-stu-id="473a6-128">The country or region name.</span></span><br/>                      |
| [<span data-ttu-id="473a6-129">**DetailLevel**</span><span class="sxs-lookup"><span data-stu-id="473a6-129">**DetailLevel**</span></span>](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | <span data-ttu-id="473a6-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473a6-130">Read-only</span></span><br/> | <span data-ttu-id="473a6-131">Nivel de detalle del informe.</span><span class="sxs-lookup"><span data-stu-id="473a6-131">The detail level for the report.</span></span><br/>                 |
| [<span data-ttu-id="473a6-132">**CódPostal**</span><span class="sxs-lookup"><span data-stu-id="473a6-132">**PostalCode**</span></span>](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | <span data-ttu-id="473a6-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473a6-133">Read-only</span></span><br/> | <span data-ttu-id="473a6-134">El código postal.</span><span class="sxs-lookup"><span data-stu-id="473a6-134">The postal code.</span></span><br/>                                 |
| [<span data-ttu-id="473a6-135">**StateProvince**</span><span class="sxs-lookup"><span data-stu-id="473a6-135">**StateProvince**</span></span>](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | <span data-ttu-id="473a6-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473a6-136">Read-only</span></span><br/> | <span data-ttu-id="473a6-137">El nombre de estado o provincia.</span><span class="sxs-lookup"><span data-stu-id="473a6-137">The state or province name.</span></span><br/>                      |
| [<span data-ttu-id="473a6-138">**Indicaciones**</span><span class="sxs-lookup"><span data-stu-id="473a6-138">**Timestamp**</span></span>](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | <span data-ttu-id="473a6-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="473a6-139">Read-only</span></span><br/> | <span data-ttu-id="473a6-140">Fecha y hora en que se generó el informe.</span><span class="sxs-lookup"><span data-stu-id="473a6-140">The date and time when the report was generated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="473a6-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="473a6-141">Remarks</span></span>

<span data-ttu-id="473a6-142">Puede recuperar este objeto a través de la propiedad [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) de un objeto [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="473a6-142">You can retrieve this object through the [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) property of a [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md) object.</span></span> <span data-ttu-id="473a6-143">Puede recibir este objeto a través del evento [**NewCivicAddressReport**](newcivicaddressreport.md) .</span><span class="sxs-lookup"><span data-stu-id="473a6-143">You can receive this object through the [**NewCivicAddressReport**](newcivicaddressreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="473a6-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="473a6-144">Requirements</span></span>



| <span data-ttu-id="473a6-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="473a6-145">Requirement</span></span> | <span data-ttu-id="473a6-146">Value</span><span class="sxs-lookup"><span data-stu-id="473a6-146">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="473a6-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="473a6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="473a6-148">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="473a6-148">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="473a6-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="473a6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="473a6-150">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="473a6-150">None supported</span></span><br/>                  |



 

