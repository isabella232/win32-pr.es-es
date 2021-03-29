---
description: Informe de latitud y longitud actual.
ms.assetid: d2bb305f-911e-46f7-abde-56e9fba9182b
title: Propiedad LocationDisp. LatLongReportFactory. LatLongReport (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.LatLongReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c44582c01685431e9b5dfa4820735728dd2a9cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277188"
---
# <a name="locationdisplatlongreportfactorylatlongreport-property"></a><span data-ttu-id="09781-103">Propiedad LocationDisp. LatLongReportFactory. LatLongReport</span><span class="sxs-lookup"><span data-stu-id="09781-103">LocationDisp.LatLongReportFactory.LatLongReport property</span></span>

<span data-ttu-id="09781-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="09781-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="09781-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="09781-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="09781-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09781-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="09781-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="09781-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="09781-108">Informe de latitud y longitud actual.</span><span class="sxs-lookup"><span data-stu-id="09781-108">The current latitude/longitude report.</span></span>

<span data-ttu-id="09781-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09781-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="09781-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09781-110">Syntax</span></span>


```JScript
objLatLongReport = LocationDisp.LatLongReportFactory.LatLongReport
```



## <a name="property-value"></a><span data-ttu-id="09781-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="09781-111">Property value</span></span>

<span data-ttu-id="09781-112">Esta propiedad es un [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09781-112">This property is a read-only [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span>

## <a name="examples"></a><span data-ttu-id="09781-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="09781-113">Examples</span></span>

<span data-ttu-id="09781-114">Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de LatLong simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="09781-114">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="09781-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09781-115">Requirements</span></span>



| <span data-ttu-id="09781-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="09781-116">Requirement</span></span> | <span data-ttu-id="09781-117">Value</span><span class="sxs-lookup"><span data-stu-id="09781-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09781-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09781-118">Minimum supported client</span></span><br/> | <span data-ttu-id="09781-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="09781-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="09781-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09781-120">Minimum supported server</span></span><br/> | <span data-ttu-id="09781-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="09781-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="09781-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09781-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="09781-123"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="09781-123"><dt>Locationapi.h</dt></span></span> </dl> |



 

