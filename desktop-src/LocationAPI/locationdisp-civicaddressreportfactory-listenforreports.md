---
description: Solicita eventos del informe de direcciones cívica.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Método LocationDisp. CivicAddressReportFactory. ListenForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003053"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a><span data-ttu-id="8f7cc-103">LocationDisp. CivicAddressReportFactory. ListenForReports, método</span><span class="sxs-lookup"><span data-stu-id="8f7cc-103">LocationDisp.CivicAddressReportFactory.ListenForReports method</span></span>

<span data-ttu-id="8f7cc-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="8f7cc-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8f7cc-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="8f7cc-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8f7cc-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f7cc-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="8f7cc-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="8f7cc-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="8f7cc-108">Solicita eventos del informe de direcciones cívica.</span><span class="sxs-lookup"><span data-stu-id="8f7cc-108">Requests civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f7cc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f7cc-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="8f7cc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f7cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f7cc-111">*requestedReportInterval*</span><span class="sxs-lookup"><span data-stu-id="8f7cc-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="8f7cc-112">Número (**palabra doble**) que representa la hora solicitada entre eventos de informe de direcciones cívica, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="8f7cc-112">Number (**double word**) representing the requested time between civic address report events, in milliseconds.</span></span> <span data-ttu-id="8f7cc-113">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="8f7cc-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f7cc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f7cc-114">Return value</span></span>

<span data-ttu-id="8f7cc-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8f7cc-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f7cc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f7cc-116">Remarks</span></span>

<span data-ttu-id="8f7cc-117">No es necesario que el proveedor de ubicación proporcione la precisión que se solicita.</span><span class="sxs-lookup"><span data-stu-id="8f7cc-117">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="8f7cc-118">Lea el valor de la propiedad [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) para detectar la configuración de intervalo de informes real.</span><span class="sxs-lookup"><span data-stu-id="8f7cc-118">Read the value of the [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="8f7cc-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8f7cc-119">Examples</span></span>

<span data-ttu-id="8f7cc-120">Para obtener un ejemplo de cómo usar este método, consulte [escucha de eventos de informe de direcciones cívica](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="8f7cc-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f7cc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f7cc-121">Requirements</span></span>



| <span data-ttu-id="8f7cc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f7cc-122">Requirement</span></span> | <span data-ttu-id="8f7cc-123">Value</span><span class="sxs-lookup"><span data-stu-id="8f7cc-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f7cc-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f7cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8f7cc-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f7cc-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8f7cc-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f7cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8f7cc-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8f7cc-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8f7cc-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f7cc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f7cc-129"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f7cc-129"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f7cc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f7cc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f7cc-131">**Evento NewCivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="8f7cc-131">**NewCivicAddressReport Event**</span></span>](newcivicaddressreport.md)
</dt> </dl>

 

