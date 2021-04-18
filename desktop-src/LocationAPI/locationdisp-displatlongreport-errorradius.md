---
description: Distancia desde la ubicación indicada, en metros. Combinado con la ubicación indicada como origen, este radio describe el círculo en el que probablemente se encuentra la ubicación real.
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: Propiedad LocationDisp. DispLatLongReport. ErrorRadius
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687702"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a><span data-ttu-id="a4b19-104">Propiedad LocationDisp. DispLatLongReport. ErrorRadius</span><span class="sxs-lookup"><span data-stu-id="a4b19-104">LocationDisp.DispLatLongReport.ErrorRadius property</span></span>

<span data-ttu-id="a4b19-105">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="a4b19-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a4b19-106">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="a4b19-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a4b19-107">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a4b19-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a4b19-108">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="a4b19-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a4b19-109">Distancia desde la ubicación indicada, en metros.</span><span class="sxs-lookup"><span data-stu-id="a4b19-109">A distance from the reported location, in meters.</span></span> <span data-ttu-id="a4b19-110">Combinado con la ubicación indicada como origen, este radio describe el círculo en el que probablemente se encuentra la ubicación real.</span><span class="sxs-lookup"><span data-stu-id="a4b19-110">Combined with the reported location as the origin, this radius describes the circle in which the actual location is probably located.</span></span>

<span data-ttu-id="a4b19-111">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a4b19-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b19-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4b19-112">Syntax</span></span>


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a><span data-ttu-id="a4b19-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a4b19-113">Property value</span></span>

<span data-ttu-id="a4b19-114">Esta propiedad es un **número** de solo lectura (punto flotante de precisión doble).</span><span class="sxs-lookup"><span data-stu-id="a4b19-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="a4b19-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a4b19-115">Examples</span></span>

<span data-ttu-id="a4b19-116">Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="a4b19-116">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b19-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4b19-117">Requirements</span></span>



| <span data-ttu-id="a4b19-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b19-118">Requirement</span></span> | <span data-ttu-id="a4b19-119">Value</span><span class="sxs-lookup"><span data-stu-id="a4b19-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="a4b19-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4b19-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b19-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a4b19-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a4b19-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4b19-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b19-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a4b19-123">None supported</span></span><br/>                  |



 

