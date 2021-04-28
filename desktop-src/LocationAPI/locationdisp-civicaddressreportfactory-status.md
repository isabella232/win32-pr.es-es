---
description: 'Propiedad LocationDisp.CivicAddressReportFactory.Status: el estado del informe actual.'
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: Propiedad LocationDisp.CivicAddressReportFactory.Status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: acb5bcfa589139e2c69e75124253f9d9a7b53a87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118503"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a><span data-ttu-id="1ce19-103">Propiedad LocationDisp.CivicAddressReportFactory.Status</span><span class="sxs-lookup"><span data-stu-id="1ce19-103">LocationDisp.CivicAddressReportFactory.Status property</span></span>

<span data-ttu-id="1ce19-104">\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.</span><span class="sxs-lookup"><span data-stu-id="1ce19-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1ce19-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="1ce19-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1ce19-106">En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1ce19-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="1ce19-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]</span><span class="sxs-lookup"><span data-stu-id="1ce19-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="1ce19-108">Estado actual del informe.</span><span class="sxs-lookup"><span data-stu-id="1ce19-108">The current report status.</span></span>

<span data-ttu-id="1ce19-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1ce19-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce19-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ce19-110">Syntax</span></span>


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="1ce19-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1ce19-111">Property value</span></span>

<span data-ttu-id="1ce19-112">Esta propiedad es un número de solo **lectura** (unsigned long).</span><span class="sxs-lookup"><span data-stu-id="1ce19-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="1ce19-113">Status</span><span class="sxs-lookup"><span data-stu-id="1ce19-113">Status</span></span>                                                                                               | <span data-ttu-id="1ce19-114">Significado</span><span class="sxs-lookup"><span data-stu-id="1ce19-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="1ce19-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce19-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="1ce19-116">Informe no admitido.</span><span class="sxs-lookup"><span data-stu-id="1ce19-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="1ce19-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce19-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="1ce19-118">Error.</span><span class="sxs-lookup"><span data-stu-id="1ce19-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="1ce19-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce19-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="1ce19-120">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="1ce19-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="1ce19-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce19-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="1ce19-122">Inicializando.</span><span class="sxs-lookup"><span data-stu-id="1ce19-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="1ce19-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="1ce19-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="1ce19-124">En ejecución.</span><span class="sxs-lookup"><span data-stu-id="1ce19-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="1ce19-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1ce19-125">Examples</span></span>

<span data-ttu-id="1ce19-126">Para obtener un ejemplo de cómo usar esta propiedad, vea [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="1ce19-126">For an example of how to use this property, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce19-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ce19-127">Requirements</span></span>



| <span data-ttu-id="1ce19-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ce19-128">Requirement</span></span> | <span data-ttu-id="1ce19-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1ce19-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="1ce19-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ce19-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce19-131">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ce19-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1ce19-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ce19-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce19-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1ce19-133">None supported</span></span><br/>                  |



 

