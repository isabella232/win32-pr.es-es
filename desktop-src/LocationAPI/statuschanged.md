---
description: Se produce cuando cambia el estado operativo de un informe.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Evento StatusChanged
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279659"
---
# <a name="statuschanged-event"></a><span data-ttu-id="c97c1-103">Evento StatusChanged</span><span class="sxs-lookup"><span data-stu-id="c97c1-103">StatusChanged event</span></span>

<span data-ttu-id="c97c1-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="c97c1-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c97c1-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="c97c1-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c97c1-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c97c1-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="c97c1-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="c97c1-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="c97c1-108">Se produce cuando cambia el estado operativo de un informe.</span><span class="sxs-lookup"><span data-stu-id="c97c1-108">Occurs when the operational status of a report changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c97c1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c97c1-109">Syntax</span></span>


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a><span data-ttu-id="c97c1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c97c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c97c1-111">*status*</span><span class="sxs-lookup"><span data-stu-id="c97c1-111">*status*</span></span> 
</dt> <dd>

<span data-ttu-id="c97c1-112">Nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="c97c1-112">The new status.</span></span>



| <span data-ttu-id="c97c1-113">Status</span><span class="sxs-lookup"><span data-stu-id="c97c1-113">Status</span></span>                                                                                               | <span data-ttu-id="c97c1-114">Significado</span><span class="sxs-lookup"><span data-stu-id="c97c1-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="c97c1-115"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="c97c1-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="c97c1-116">No se admite el informe.</span><span class="sxs-lookup"><span data-stu-id="c97c1-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="c97c1-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c97c1-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c97c1-118">Error.</span><span class="sxs-lookup"><span data-stu-id="c97c1-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="c97c1-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c97c1-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c97c1-120">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c97c1-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="c97c1-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c97c1-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c97c1-122">Inicializando.</span><span class="sxs-lookup"><span data-stu-id="c97c1-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="c97c1-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c97c1-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c97c1-124">En ejecución.</span><span class="sxs-lookup"><span data-stu-id="c97c1-124">Running.</span></span><br/>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c97c1-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c97c1-125">Return value</span></span>

<span data-ttu-id="c97c1-126">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="c97c1-126">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c97c1-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c97c1-127">Remarks</span></span>

<span data-ttu-id="c97c1-128">Debe implementar controladores de informes de cambio de estado independientes para los informes de direcciones cívicas y los informes de latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="c97c1-128">You should implement separate status change report handlers for civic address reports and latitude/longitude reports.</span></span>

## <a name="examples"></a><span data-ttu-id="c97c1-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c97c1-129">Examples</span></span>

<span data-ttu-id="c97c1-130">Para obtener un ejemplo de cómo usar este evento, consulte [escucha de eventos de informe de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="c97c1-130">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="c97c1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c97c1-131">Requirements</span></span>



| <span data-ttu-id="c97c1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c97c1-132">Requirement</span></span> | <span data-ttu-id="c97c1-133">Value</span><span class="sxs-lookup"><span data-stu-id="c97c1-133">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="c97c1-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c97c1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c97c1-135">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c97c1-135">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c97c1-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c97c1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c97c1-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c97c1-137">None supported</span></span><br/>                  |



 

