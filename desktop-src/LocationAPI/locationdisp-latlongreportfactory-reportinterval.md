---
description: El intervalo de eventos de informe de latitud y longitud actual en milisegundos.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Propiedad LocationDisp. LatLongReportFactory. ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277378"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a><span data-ttu-id="e267a-103">Propiedad LocationDisp. LatLongReportFactory. ReportInterval</span><span class="sxs-lookup"><span data-stu-id="e267a-103">LocationDisp.LatLongReportFactory.ReportInterval property</span></span>

<span data-ttu-id="e267a-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="e267a-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e267a-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="e267a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e267a-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e267a-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e267a-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="e267a-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e267a-108">El intervalo de eventos de informe de latitud y longitud actual en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="e267a-108">The current latitude/longitude report event interval in milliseconds.</span></span>

<span data-ttu-id="e267a-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e267a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e267a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e267a-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="e267a-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e267a-111">Property value</span></span>

<span data-ttu-id="e267a-112">Esta propiedad es de lectura/escritura **ULong**.</span><span class="sxs-lookup"><span data-stu-id="e267a-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e267a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e267a-113">Remarks</span></span>

<span data-ttu-id="e267a-114">Este valor es una solicitud al proveedor de ubicación.</span><span class="sxs-lookup"><span data-stu-id="e267a-114">This value is a request to the location provider.</span></span> <span data-ttu-id="e267a-115">No es necesario que el proveedor de ubicación proporcione informes en el intervalo que solicite.</span><span class="sxs-lookup"><span data-stu-id="e267a-115">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="e267a-116">Lea el valor de esta propiedad para detectar la configuración de intervalo de informes real.</span><span class="sxs-lookup"><span data-stu-id="e267a-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="e267a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e267a-117">Requirements</span></span>



| <span data-ttu-id="e267a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e267a-118">Requirement</span></span> | <span data-ttu-id="e267a-119">Value</span><span class="sxs-lookup"><span data-stu-id="e267a-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="e267a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e267a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e267a-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e267a-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e267a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e267a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e267a-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e267a-123">None supported</span></span><br/>                  |



 

