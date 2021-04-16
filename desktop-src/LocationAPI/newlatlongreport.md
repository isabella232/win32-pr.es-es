---
description: Se produce cuando se genera un nuevo informe de latitud y longitud.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Evento NewLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: ea305d17169b71d183a8d453e9885d8de878b026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678601"
---
# <a name="newlatlongreport-event"></a><span data-ttu-id="1d1dc-103">Evento NewLatLongReport</span><span class="sxs-lookup"><span data-stu-id="1d1dc-103">NewLatLongReport event</span></span>

<span data-ttu-id="1d1dc-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="1d1dc-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1d1dc-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="1d1dc-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1d1dc-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d1dc-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="1d1dc-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="1d1dc-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="1d1dc-108">Se produce cuando se genera un nuevo informe de latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="1d1dc-108">Occurs when a new latitude/longitude report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d1dc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d1dc-109">Syntax</span></span>


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="1d1dc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d1dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d1dc-111">*newReport*</span><span class="sxs-lookup"><span data-stu-id="1d1dc-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="1d1dc-112">El nuevo objeto [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md) .</span><span class="sxs-lookup"><span data-stu-id="1d1dc-112">The new [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d1dc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d1dc-113">Return value</span></span>

<span data-ttu-id="1d1dc-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="1d1dc-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="1d1dc-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1d1dc-115">Examples</span></span>

<span data-ttu-id="1d1dc-116">Para obtener un ejemplo de cómo usar este evento, consulte [escucha de eventos de informe de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="1d1dc-116">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d1dc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d1dc-117">Requirements</span></span>



| <span data-ttu-id="1d1dc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d1dc-118">Requirement</span></span> | <span data-ttu-id="1d1dc-119">Value</span><span class="sxs-lookup"><span data-stu-id="1d1dc-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="1d1dc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d1dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1d1dc-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d1dc-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1d1dc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d1dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1d1dc-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1d1dc-123">None supported</span></span><br/>                  |



 

