---
description: Estado actual del informe.
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: LocationDisp. LatLongReportFactory. status (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: c32f1e58c5c519bdbdf797f81f11a449bfb3dc1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360805"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a><span data-ttu-id="5d7d1-103">LocationDisp. LatLongReportFactory. status (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5d7d1-103">LocationDisp.LatLongReportFactory.Status property</span></span>

<span data-ttu-id="5d7d1-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5d7d1-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d7d1-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="5d7d1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5d7d1-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d7d1-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="5d7d1-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="5d7d1-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="5d7d1-108">Estado actual del informe.</span><span class="sxs-lookup"><span data-stu-id="5d7d1-108">The current report status.</span></span>

<span data-ttu-id="5d7d1-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5d7d1-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7d1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d7d1-110">Syntax</span></span>


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="5d7d1-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5d7d1-111">Property value</span></span>

<span data-ttu-id="5d7d1-112">Esta propiedad es un **número** de solo lectura (unsigned Long).</span><span class="sxs-lookup"><span data-stu-id="5d7d1-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="5d7d1-113">Status</span><span class="sxs-lookup"><span data-stu-id="5d7d1-113">Status</span></span>                                                                                               | <span data-ttu-id="5d7d1-114">Significado</span><span class="sxs-lookup"><span data-stu-id="5d7d1-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="5d7d1-115"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="5d7d1-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="5d7d1-116">No se admite el informe.</span><span class="sxs-lookup"><span data-stu-id="5d7d1-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="5d7d1-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="5d7d1-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="5d7d1-118">Error.</span><span class="sxs-lookup"><span data-stu-id="5d7d1-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="5d7d1-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="5d7d1-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="5d7d1-120">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="5d7d1-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="5d7d1-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="5d7d1-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="5d7d1-122">Inicializando.</span><span class="sxs-lookup"><span data-stu-id="5d7d1-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="5d7d1-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="5d7d1-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="5d7d1-124">En ejecución.</span><span class="sxs-lookup"><span data-stu-id="5d7d1-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="5d7d1-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5d7d1-125">Examples</span></span>

<span data-ttu-id="5d7d1-126">Para obtener un ejemplo de cómo usar esta propiedad, consulte [escucha de eventos de informe de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="5d7d1-126">For an example of how to use this property, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7d1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d7d1-127">Requirements</span></span>



| <span data-ttu-id="5d7d1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d7d1-128">Requirement</span></span> | <span data-ttu-id="5d7d1-129">Value</span><span class="sxs-lookup"><span data-stu-id="5d7d1-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="5d7d1-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d7d1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7d1-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d7d1-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5d7d1-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d7d1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7d1-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5d7d1-133">None supported</span></span><br/>                  |



 

