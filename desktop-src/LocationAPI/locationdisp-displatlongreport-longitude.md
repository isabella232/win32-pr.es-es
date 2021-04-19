---
description: Longitud actual, en grados.
ms.assetid: f4fa1cbb-d682-42ab-9dd8-dff636ea4c8a
title: Propiedad LocationDisp. DispLatLongReport. longitude
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Longitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: c705ebd9476582f05b6dc87233dcc8e8990c5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688642"
---
# <a name="locationdispdisplatlongreportlongitude-property"></a><span data-ttu-id="a72ba-103">Propiedad LocationDisp. DispLatLongReport. longitude</span><span class="sxs-lookup"><span data-stu-id="a72ba-103">LocationDisp.DispLatLongReport.Longitude property</span></span>

<span data-ttu-id="a72ba-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a72ba-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a72ba-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="a72ba-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a72ba-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a72ba-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a72ba-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="a72ba-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a72ba-108">Longitud actual, en grados.</span><span class="sxs-lookup"><span data-stu-id="a72ba-108">Current longitude, in degrees.</span></span> <span data-ttu-id="a72ba-109">La longitud está comprendida entre-180 y 180, donde este es positivo.</span><span class="sxs-lookup"><span data-stu-id="a72ba-109">The longitude is between -180 and 180, where east is positive.</span></span>

<span data-ttu-id="a72ba-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a72ba-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a72ba-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a72ba-111">Syntax</span></span>


```JScript
Longitude = LocationDisp.DispLatLongReport.Longitude
```



## <a name="property-value"></a><span data-ttu-id="a72ba-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a72ba-112">Property value</span></span>

<span data-ttu-id="a72ba-113">Esta propiedad es un **número** de solo lectura (punto flotante de precisión doble).</span><span class="sxs-lookup"><span data-stu-id="a72ba-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="a72ba-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a72ba-114">Examples</span></span>

<span data-ttu-id="a72ba-115">Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="a72ba-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="a72ba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a72ba-116">Requirements</span></span>



| <span data-ttu-id="a72ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a72ba-117">Requirement</span></span> | <span data-ttu-id="a72ba-118">Value</span><span class="sxs-lookup"><span data-stu-id="a72ba-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="a72ba-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a72ba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a72ba-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a72ba-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a72ba-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a72ba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a72ba-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a72ba-122">None supported</span></span><br/>                  |



 

