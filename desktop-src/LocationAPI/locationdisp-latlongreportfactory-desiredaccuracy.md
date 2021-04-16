---
description: Valor de precisión deseado actual.
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: Propiedad LocationDisp. LatLongReportFactory. DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: e17e415d9503660d873ae4df67d2469c646dd80e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678473"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a><span data-ttu-id="440d0-103">Propiedad LocationDisp. LatLongReportFactory. DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="440d0-103">LocationDisp.LatLongReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="440d0-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="440d0-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="440d0-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="440d0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="440d0-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="440d0-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="440d0-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="440d0-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="440d0-108">Valor de precisión deseado actual.</span><span class="sxs-lookup"><span data-stu-id="440d0-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="440d0-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="440d0-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="440d0-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="440d0-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="440d0-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="440d0-111">Property value</span></span>

<span data-ttu-id="440d0-112">Esta propiedad es de lectura/escritura **ULong**.</span><span class="sxs-lookup"><span data-stu-id="440d0-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="440d0-113">Value</span><span class="sxs-lookup"><span data-stu-id="440d0-113">Value</span></span>                                                                        | <span data-ttu-id="440d0-114">Significado</span><span class="sxs-lookup"><span data-stu-id="440d0-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="440d0-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="440d0-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="440d0-116">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="440d0-116">Default.</span></span> <span data-ttu-id="440d0-117">El sensor debe utilizar la precisión para la que puede optimizar el uso de energía y otras consideraciones de costo.</span><span class="sxs-lookup"><span data-stu-id="440d0-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="440d0-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="440d0-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="440d0-119">El sensor debe proporcionar el informe más preciso posible.</span><span class="sxs-lookup"><span data-stu-id="440d0-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="440d0-120">Para ello, pueden usarse servicios que no son gratuitos o aumentar el consumo de energía de la batería o del ancho de banda de la conexión.</span><span class="sxs-lookup"><span data-stu-id="440d0-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="440d0-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="440d0-121">Remarks</span></span>

<span data-ttu-id="440d0-122">Este valor es una solicitud al proveedor de ubicación.</span><span class="sxs-lookup"><span data-stu-id="440d0-122">This value is a request to the location provider.</span></span> <span data-ttu-id="440d0-123">No es necesario que el proveedor de ubicación proporcione informes en el intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="440d0-123">The location provider is not required to provide reports at the interval you requested.</span></span> <span data-ttu-id="440d0-124">Lea el valor de esta propiedad para detectar la configuración de intervalo de informes real.</span><span class="sxs-lookup"><span data-stu-id="440d0-124">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="440d0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="440d0-125">Requirements</span></span>



| <span data-ttu-id="440d0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="440d0-126">Requirement</span></span> | <span data-ttu-id="440d0-127">Value</span><span class="sxs-lookup"><span data-stu-id="440d0-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="440d0-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="440d0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="440d0-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="440d0-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="440d0-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="440d0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="440d0-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="440d0-131">None supported</span></span><br/>                  |



 

