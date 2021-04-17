---
description: El informe de dirección cívica actual.
ms.assetid: a58dd612-bc54-42d1-9960-8c3de1c4fa83
title: Propiedad LocationDisp. CivicAddressReportFactory. CivicAddressReport (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.CivicAddressReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c8be6e03861f1c5b2abffcb4b23d4845defa494e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688116"
---
# <a name="locationdispcivicaddressreportfactorycivicaddressreport-property"></a><span data-ttu-id="4437d-103">Propiedad LocationDisp. CivicAddressReportFactory. CivicAddressReport</span><span class="sxs-lookup"><span data-stu-id="4437d-103">LocationDisp.CivicAddressReportFactory.CivicAddressReport property</span></span>

<span data-ttu-id="4437d-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4437d-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4437d-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="4437d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="4437d-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4437d-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="4437d-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="4437d-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="4437d-108">El informe de dirección cívica actual.</span><span class="sxs-lookup"><span data-stu-id="4437d-108">The current civic address report.</span></span>

<span data-ttu-id="4437d-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4437d-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4437d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4437d-110">Syntax</span></span>


```JScript
objCivicAddressReport = LocationDisp.CivicAddressReportFactory.CivicAddressReport
```



## <a name="property-value"></a><span data-ttu-id="4437d-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4437d-111">Property value</span></span>

<span data-ttu-id="4437d-112">Esta propiedad es un [**LocationDisp. CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md)de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4437d-112">This property is a read-only [**LocationDisp.CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4437d-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4437d-113">Examples</span></span>

<span data-ttu-id="4437d-114">Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de dirección cívica simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="4437d-114">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="4437d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4437d-115">Requirements</span></span>



| <span data-ttu-id="4437d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4437d-116">Requirement</span></span> | <span data-ttu-id="4437d-117">Value</span><span class="sxs-lookup"><span data-stu-id="4437d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4437d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4437d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4437d-119">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4437d-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4437d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4437d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4437d-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4437d-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4437d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4437d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4437d-123"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4437d-123"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4437d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="4437d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4437d-125">**LocationDisp.CivicAddressReportFactory**</span><span class="sxs-lookup"><span data-stu-id="4437d-125">**LocationDisp.CivicAddressReportFactory**</span></span>](locationdisp-civicaddressreportfactory.md)
</dt> </dl>

 

