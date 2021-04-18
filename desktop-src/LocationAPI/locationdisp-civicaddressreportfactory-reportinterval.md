---
description: El intervalo de eventos del informe de dirección cívica actual en milisegundos.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: Propiedad LocationDisp. CivicAddressReportFactory. ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: 47f7840be20ac640b5a8e7014f8401bc2350d328
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688645"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a><span data-ttu-id="e3c8b-103">Propiedad LocationDisp. CivicAddressReportFactory. ReportInterval</span><span class="sxs-lookup"><span data-stu-id="e3c8b-103">LocationDisp.CivicAddressReportFactory.ReportInterval property</span></span>

<span data-ttu-id="e3c8b-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e3c8b-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e3c8b-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e3c8b-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="e3c8b-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="e3c8b-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="e3c8b-108">El intervalo de eventos del informe de dirección cívica actual en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-108">The current civic address report event interval in milliseconds.</span></span>

<span data-ttu-id="e3c8b-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c8b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3c8b-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="e3c8b-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e3c8b-111">Property value</span></span>

<span data-ttu-id="e3c8b-112">Esta propiedad es de lectura/escritura **ULong**.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c8b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3c8b-113">Remarks</span></span>

<span data-ttu-id="e3c8b-114">Este valor es una solicitud para el proveedor de ubicación.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-114">This value is a request for the location provider.</span></span> <span data-ttu-id="e3c8b-115">No es necesario que el proveedor de ubicación proporcione informes en el intervalo solicitado.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-115">The location provider is not required to provide reports at the interval that you requested.</span></span> <span data-ttu-id="e3c8b-116">Lea el valor de esta propiedad para detectar la configuración de intervalo de informes real.</span><span class="sxs-lookup"><span data-stu-id="e3c8b-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c8b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3c8b-117">Requirements</span></span>



| <span data-ttu-id="e3c8b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3c8b-118">Requirement</span></span> | <span data-ttu-id="e3c8b-119">Value</span><span class="sxs-lookup"><span data-stu-id="e3c8b-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="e3c8b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3c8b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3c8b-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3c8b-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e3c8b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3c8b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3c8b-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e3c8b-123">None supported</span></span><br/>                  |



 

