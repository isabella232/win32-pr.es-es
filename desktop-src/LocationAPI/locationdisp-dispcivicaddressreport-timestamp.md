---
description: Fecha y hora en que se generó el informe.
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: Propiedad LocationDisp. DispCivicAddressReport. timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b805454a6c2d62a58ba5a2a3de8f5b5095e1db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688546"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a><span data-ttu-id="5aadd-103">Propiedad LocationDisp. DispCivicAddressReport. timestamp</span><span class="sxs-lookup"><span data-stu-id="5aadd-103">LocationDisp.DispCivicAddressReport.Timestamp property</span></span>

<span data-ttu-id="5aadd-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="5aadd-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5aadd-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="5aadd-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5aadd-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5aadd-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="5aadd-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="5aadd-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="5aadd-108">Fecha y hora en que se generó el informe.</span><span class="sxs-lookup"><span data-stu-id="5aadd-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="5aadd-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aadd-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aadd-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aadd-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="5aadd-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5aadd-111">Property value</span></span>

<span data-ttu-id="5aadd-112">Esta propiedad es una **fecha** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5aadd-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="5aadd-113">Las marcas de tiempo se proporcionan como hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="5aadd-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="5aadd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aadd-114">Remarks</span></span>

<span data-ttu-id="5aadd-115">Tenga en cuenta que los lenguajes de scripting, como Microsoft JScript, pueden requerir que realice conversiones a otros formatos de hora al mostrar las marcas de tiempo como cadenas.</span><span class="sxs-lookup"><span data-stu-id="5aadd-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="5aadd-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5aadd-116">Examples</span></span>

<span data-ttu-id="5aadd-117">Para obtener un ejemplo de cómo usar esta propiedad, vea [un ejemplo de informe de dirección cívica simple](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="5aadd-117">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aadd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aadd-118">Requirements</span></span>



| <span data-ttu-id="5aadd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aadd-119">Requirement</span></span> | <span data-ttu-id="5aadd-120">Value</span><span class="sxs-lookup"><span data-stu-id="5aadd-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="5aadd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aadd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5aadd-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5aadd-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5aadd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aadd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5aadd-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5aadd-124">None supported</span></span><br/>                  |



 

