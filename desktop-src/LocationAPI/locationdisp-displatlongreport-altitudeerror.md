---
description: Error de altitud, en metros.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Propiedad LocationDisp. DispLatLongReport. AltitudeError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910990"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a><span data-ttu-id="9c276-103">Propiedad LocationDisp. DispLatLongReport. AltitudeError</span><span class="sxs-lookup"><span data-stu-id="9c276-103">LocationDisp.DispLatLongReport.AltitudeError property</span></span>

<span data-ttu-id="9c276-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="9c276-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9c276-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="9c276-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9c276-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c276-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="9c276-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="9c276-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="9c276-108">Error de altitud, en metros.</span><span class="sxs-lookup"><span data-stu-id="9c276-108">Altitude error, in meters.</span></span>

<span data-ttu-id="9c276-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9c276-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c276-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c276-110">Syntax</span></span>


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a><span data-ttu-id="9c276-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9c276-111">Property value</span></span>

<span data-ttu-id="9c276-112">Esta propiedad es un **número** de solo lectura (punto flotante de precisión doble).</span><span class="sxs-lookup"><span data-stu-id="9c276-112">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c276-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c276-113">Remarks</span></span>

<span data-ttu-id="9c276-114">No es necesario que los sensores de ubicación proporcionen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9c276-114">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="9c276-115">Debe controlar las excepciones al intentar tener acceso a esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9c276-115">You should handle exceptions when attempting to access this property.</span></span>

## <a name="examples"></a><span data-ttu-id="9c276-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9c276-116">Examples</span></span>

<span data-ttu-id="9c276-117">Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="9c276-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c276-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c276-118">Requirements</span></span>



| <span data-ttu-id="9c276-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c276-119">Requirement</span></span> | <span data-ttu-id="9c276-120">Value</span><span class="sxs-lookup"><span data-stu-id="9c276-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="9c276-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c276-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9c276-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c276-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9c276-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c276-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9c276-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9c276-124">None supported</span></span><br/>                  |



 

