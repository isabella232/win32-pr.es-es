---
description: Latitud actual, en grados.
ms.assetid: 24a4e75c-5162-406a-bf34-471387bff5d9
title: Propiedad LocationDisp. DispLatLongReport. Latitude
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Latitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7f1bb6e7441b4e007c972f43bb45f59236ebe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678315"
---
# <a name="locationdispdisplatlongreportlatitude-property"></a><span data-ttu-id="5f85d-103">Propiedad LocationDisp. DispLatLongReport. Latitude</span><span class="sxs-lookup"><span data-stu-id="5f85d-103">LocationDisp.DispLatLongReport.Latitude property</span></span>

<span data-ttu-id="5f85d-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5f85d-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5f85d-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="5f85d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5f85d-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5f85d-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="5f85d-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="5f85d-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="5f85d-108">Latitud actual, en grados.</span><span class="sxs-lookup"><span data-stu-id="5f85d-108">Current latitude, in degrees.</span></span> <span data-ttu-id="5f85d-109">La latitud está entre-90 y 90, donde norte es positivo.</span><span class="sxs-lookup"><span data-stu-id="5f85d-109">The latitude is between -90 and 90, where north is positive.</span></span>

<span data-ttu-id="5f85d-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f85d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f85d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f85d-111">Syntax</span></span>


```JScript
Latitude = LocationDisp.DispLatLongReport.Latitude
```



## <a name="property-value"></a><span data-ttu-id="5f85d-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5f85d-112">Property value</span></span>

<span data-ttu-id="5f85d-113">Esta propiedad es un **número** de solo lectura (punto flotante de precisión doble).</span><span class="sxs-lookup"><span data-stu-id="5f85d-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="5f85d-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5f85d-114">Examples</span></span>

<span data-ttu-id="5f85d-115">Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="5f85d-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f85d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f85d-116">Requirements</span></span>



| <span data-ttu-id="5f85d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f85d-117">Requirement</span></span> | <span data-ttu-id="5f85d-118">Value</span><span class="sxs-lookup"><span data-stu-id="5f85d-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="5f85d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f85d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5f85d-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f85d-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5f85d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f85d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5f85d-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5f85d-122">None supported</span></span><br/>                  |



 

