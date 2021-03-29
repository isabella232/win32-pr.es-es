---
description: Solicita eventos de informe de latitud y longitud.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: Método LocationDisp. LatLongReportFactory. ListenForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814806"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a><span data-ttu-id="2fbdc-103">LocationDisp. LatLongReportFactory. ListenForReports, método</span><span class="sxs-lookup"><span data-stu-id="2fbdc-103">LocationDisp.LatLongReportFactory.ListenForReports method</span></span>

<span data-ttu-id="2fbdc-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="2fbdc-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2fbdc-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="2fbdc-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2fbdc-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2fbdc-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="2fbdc-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="2fbdc-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="2fbdc-108">Solicita eventos de informe de latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="2fbdc-108">Requests latitude/longitude report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fbdc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fbdc-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="2fbdc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fbdc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fbdc-111">*requestedReportInterval*</span><span class="sxs-lookup"><span data-stu-id="2fbdc-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="2fbdc-112">Número (**palabra doble**) que representa el tiempo solicitado entre los eventos de informe de latitud y longitud, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="2fbdc-112">Number (**double word**) representing the requested time between latitude/longitude report events, in milliseconds.</span></span> <span data-ttu-id="2fbdc-113">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2fbdc-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fbdc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fbdc-114">Return value</span></span>

<span data-ttu-id="2fbdc-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2fbdc-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fbdc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fbdc-116">Remarks</span></span>

<span data-ttu-id="2fbdc-117">No es necesario que el proveedor de ubicación proporcione informes en el intervalo que solicite.</span><span class="sxs-lookup"><span data-stu-id="2fbdc-117">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="2fbdc-118">Lea el valor de la propiedad [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) para detectar la configuración de intervalo de informes real.</span><span class="sxs-lookup"><span data-stu-id="2fbdc-118">Read the value of the [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="2fbdc-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2fbdc-119">Examples</span></span>

<span data-ttu-id="2fbdc-120">Para obtener un ejemplo de cómo usar este método, consulte [escucha de eventos de informe de LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="2fbdc-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fbdc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fbdc-121">Requirements</span></span>



| <span data-ttu-id="2fbdc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fbdc-122">Requirement</span></span> | <span data-ttu-id="2fbdc-123">Value</span><span class="sxs-lookup"><span data-stu-id="2fbdc-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fbdc-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fbdc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2fbdc-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fbdc-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2fbdc-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fbdc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2fbdc-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2fbdc-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2fbdc-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fbdc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fbdc-129"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fbdc-129"><dt>Locationapi.h</dt></span></span> </dl> |



 

