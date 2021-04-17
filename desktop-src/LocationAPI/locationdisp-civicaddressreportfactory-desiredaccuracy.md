---
description: Valor de precisión deseado actual.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Propiedad LocationDisp. CivicAddressReportFactory. DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: eb05aeb6a69bfe978682d418cf1e71aed2184bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669855"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a><span data-ttu-id="63652-103">Propiedad LocationDisp. CivicAddressReportFactory. DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="63652-103">LocationDisp.CivicAddressReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="63652-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="63652-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="63652-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="63652-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="63652-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="63652-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="63652-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="63652-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="63652-108">Valor de precisión deseado actual.</span><span class="sxs-lookup"><span data-stu-id="63652-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="63652-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="63652-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="63652-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63652-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="63652-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="63652-111">Property value</span></span>

<span data-ttu-id="63652-112">Esta propiedad es de lectura/escritura **ULong**.</span><span class="sxs-lookup"><span data-stu-id="63652-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="63652-113">Value</span><span class="sxs-lookup"><span data-stu-id="63652-113">Value</span></span>                                                                        | <span data-ttu-id="63652-114">Significado</span><span class="sxs-lookup"><span data-stu-id="63652-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63652-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63652-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="63652-116">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="63652-116">Default.</span></span> <span data-ttu-id="63652-117">El sensor debe utilizar la precisión para la que puede optimizar el uso de energía y otras consideraciones de costo.</span><span class="sxs-lookup"><span data-stu-id="63652-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="63652-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="63652-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="63652-119">El sensor debe proporcionar el informe más preciso posible.</span><span class="sxs-lookup"><span data-stu-id="63652-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="63652-120">Para ello, pueden usarse servicios que no son gratuitos o aumentar el consumo de energía de la batería o del ancho de banda de la conexión.</span><span class="sxs-lookup"><span data-stu-id="63652-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63652-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63652-121">Remarks</span></span>

<span data-ttu-id="63652-122">Este valor es una solicitud al proveedor de ubicación.</span><span class="sxs-lookup"><span data-stu-id="63652-122">This value is a request to the location provider.</span></span> <span data-ttu-id="63652-123">No es necesario que el proveedor de ubicación proporcione la precisión que se solicita.</span><span class="sxs-lookup"><span data-stu-id="63652-123">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="63652-124">Lea el valor de esta propiedad para detectar la configuración de precisión verdadera.</span><span class="sxs-lookup"><span data-stu-id="63652-124">Read the value of this property to discover the true accuracy setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="63652-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63652-125">Requirements</span></span>



| <span data-ttu-id="63652-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="63652-126">Requirement</span></span> | <span data-ttu-id="63652-127">Value</span><span class="sxs-lookup"><span data-stu-id="63652-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="63652-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63652-128">Minimum supported client</span></span><br/> | <span data-ttu-id="63652-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="63652-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="63652-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63652-130">Minimum supported server</span></span><br/> | <span data-ttu-id="63652-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="63652-131">None supported</span></span><br/>                  |



 

