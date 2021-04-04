---
description: Altitud actual, en metros. La altitud es relativa al Elipsoide de referencia.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: Propiedad LocationDisp. DispLatLongReport. altitud
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910097"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a><span data-ttu-id="b63be-104">Propiedad LocationDisp. DispLatLongReport. altitud</span><span class="sxs-lookup"><span data-stu-id="b63be-104">LocationDisp.DispLatLongReport.Altitude property</span></span>

<span data-ttu-id="b63be-105">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b63be-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b63be-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="b63be-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b63be-107">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b63be-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b63be-108">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="b63be-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b63be-109">Altitud actual, en metros.</span><span class="sxs-lookup"><span data-stu-id="b63be-109">Current altitude, in meters.</span></span> <span data-ttu-id="b63be-110">La altitud es relativa al Elipsoide de referencia.</span><span class="sxs-lookup"><span data-stu-id="b63be-110">Altitude is relative to the reference ellipsoid.</span></span>

<span data-ttu-id="b63be-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b63be-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b63be-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b63be-112">Syntax</span></span>


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a><span data-ttu-id="b63be-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b63be-113">Property value</span></span>

<span data-ttu-id="b63be-114">Esta propiedad es un **número** de solo lectura (punto flotante de precisión doble).</span><span class="sxs-lookup"><span data-stu-id="b63be-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="b63be-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b63be-115">Remarks</span></span>

<span data-ttu-id="b63be-116">No es necesario que los sensores de ubicación proporcionen esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b63be-116">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="b63be-117">Debe controlar las excepciones al intentar tener acceso a esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b63be-117">You should handle exceptions when attempting to access this property.</span></span>

<span data-ttu-id="b63be-118">El método **altitud** recupera la altitud en relación con la Elipsoide de referencia definida por la última revisión del sistema geodésico mundial (WGS 84), en lugar de la altitud relativa al nivel del mar.</span><span class="sxs-lookup"><span data-stu-id="b63be-118">The **Altitude** method retrieves the altitude relative to the reference ellipsoid that is defined by the latest revision of the World Geodetic System (WGS 84), rather than the altitude relative to sea level.</span></span>

## <a name="examples"></a><span data-ttu-id="b63be-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b63be-119">Examples</span></span>

<span data-ttu-id="b63be-120">Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="b63be-120">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="b63be-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b63be-121">Requirements</span></span>



| <span data-ttu-id="b63be-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b63be-122">Requirement</span></span> | <span data-ttu-id="b63be-123">Value</span><span class="sxs-lookup"><span data-stu-id="b63be-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="b63be-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b63be-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b63be-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b63be-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b63be-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b63be-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b63be-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b63be-127">None supported</span></span><br/>                  |



 

