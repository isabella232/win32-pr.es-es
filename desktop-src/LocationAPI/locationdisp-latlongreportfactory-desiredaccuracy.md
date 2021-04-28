---
description: 'Propiedad LocationDisp.LatLongReportFactory.DesiredAccuracy: el valor actual de precisión deseada.'
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: Propiedad LocationDisp.LatLongReportFactory.DesiredAccuracy
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
ms.openlocfilehash: afc5ec235df6c9e07a665410cb09e00f24305304
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088973"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a><span data-ttu-id="3a200-103">Propiedad LocationDisp.LatLongReportFactory.DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="3a200-103">LocationDisp.LatLongReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="3a200-104">\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.</span><span class="sxs-lookup"><span data-stu-id="3a200-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3a200-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="3a200-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="3a200-106">En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a200-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="3a200-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]</span><span class="sxs-lookup"><span data-stu-id="3a200-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="3a200-108">Valor actual de precisión deseada.</span><span class="sxs-lookup"><span data-stu-id="3a200-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="3a200-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3a200-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a200-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a200-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="3a200-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3a200-111">Property value</span></span>

<span data-ttu-id="3a200-112">Esta propiedad es un ULONG de **lectura y escritura.**</span><span class="sxs-lookup"><span data-stu-id="3a200-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="3a200-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3a200-113">Value</span></span>                                                                        | <span data-ttu-id="3a200-114">Significado</span><span class="sxs-lookup"><span data-stu-id="3a200-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3a200-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3a200-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="3a200-116">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3a200-116">Default.</span></span> <span data-ttu-id="3a200-117">El sensor debe usar la precisión para la que puede optimizar el uso de energía y otras consideraciones de costos.</span><span class="sxs-lookup"><span data-stu-id="3a200-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="3a200-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3a200-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="3a200-119">El sensor debe proporcionar el informe más preciso posible.</span><span class="sxs-lookup"><span data-stu-id="3a200-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="3a200-120">Para ello, pueden usarse servicios que no son gratuitos o aumentar el consumo de energía de la batería o del ancho de banda de la conexión.</span><span class="sxs-lookup"><span data-stu-id="3a200-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a200-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3a200-121">Remarks</span></span>

<span data-ttu-id="3a200-122">Este valor es una solicitud al proveedor de ubicación.</span><span class="sxs-lookup"><span data-stu-id="3a200-122">This value is a request to the location provider.</span></span> <span data-ttu-id="3a200-123">No es necesario que el proveedor de ubicación proporcione informes en el intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="3a200-123">The location provider is not required to provide reports at the interval you requested.</span></span> <span data-ttu-id="3a200-124">Lea el valor de esta propiedad para detectar la configuración verdadera del intervalo de informe.</span><span class="sxs-lookup"><span data-stu-id="3a200-124">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a200-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a200-125">Requirements</span></span>



| <span data-ttu-id="3a200-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a200-126">Requirement</span></span> | <span data-ttu-id="3a200-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3a200-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="3a200-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a200-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3a200-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a200-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3a200-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a200-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3a200-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3a200-131">None supported</span></span><br/>                  |



 

