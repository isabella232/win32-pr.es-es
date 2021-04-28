---
description: 'Propiedad LocationDisp.LatLongReportFactory.Status: el estado del informe actual.'
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: Propiedad LocationDisp.LatLongReportFactory.Status
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
ms.openlocfilehash: 37e66c3f289f5376b31ffe516f45d79f2fef51e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088903"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a><span data-ttu-id="51fab-103">Propiedad LocationDisp.LatLongReportFactory.Status</span><span class="sxs-lookup"><span data-stu-id="51fab-103">LocationDisp.LatLongReportFactory.Status property</span></span>

<span data-ttu-id="51fab-104">\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.</span><span class="sxs-lookup"><span data-stu-id="51fab-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="51fab-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="51fab-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="51fab-106">En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="51fab-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="51fab-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]</span><span class="sxs-lookup"><span data-stu-id="51fab-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="51fab-108">Estado actual del informe.</span><span class="sxs-lookup"><span data-stu-id="51fab-108">The current report status.</span></span>

<span data-ttu-id="51fab-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="51fab-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fab-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51fab-110">Syntax</span></span>


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="51fab-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="51fab-111">Property value</span></span>

<span data-ttu-id="51fab-112">Esta propiedad es un número de solo **lectura** (unsigned long).</span><span class="sxs-lookup"><span data-stu-id="51fab-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="51fab-113">Status</span><span class="sxs-lookup"><span data-stu-id="51fab-113">Status</span></span>                                                                                               | <span data-ttu-id="51fab-114">Significado</span><span class="sxs-lookup"><span data-stu-id="51fab-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="51fab-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="51fab-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="51fab-116">Informe no admitido.</span><span class="sxs-lookup"><span data-stu-id="51fab-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="51fab-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="51fab-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="51fab-118">Error.</span><span class="sxs-lookup"><span data-stu-id="51fab-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="51fab-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="51fab-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="51fab-120">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="51fab-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="51fab-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="51fab-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="51fab-122">Inicializando.</span><span class="sxs-lookup"><span data-stu-id="51fab-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="51fab-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="51fab-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="51fab-124">En ejecución.</span><span class="sxs-lookup"><span data-stu-id="51fab-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="51fab-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="51fab-125">Examples</span></span>

<span data-ttu-id="51fab-126">Para obtener un ejemplo de cómo usar esta propiedad, vea [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="51fab-126">For an example of how to use this property, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="51fab-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51fab-127">Requirements</span></span>



| <span data-ttu-id="51fab-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="51fab-128">Requirement</span></span> | <span data-ttu-id="51fab-129">Valor</span><span class="sxs-lookup"><span data-stu-id="51fab-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="51fab-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51fab-130">Minimum supported client</span></span><br/> | <span data-ttu-id="51fab-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="51fab-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="51fab-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51fab-132">Minimum supported server</span></span><br/> | <span data-ttu-id="51fab-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="51fab-133">None supported</span></span><br/>                  |



 

