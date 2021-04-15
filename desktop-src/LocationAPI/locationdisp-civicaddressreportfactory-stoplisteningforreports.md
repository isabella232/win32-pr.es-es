---
description: Detiene los eventos del informe de direcciones cívica.
ms.assetid: 6efe26bc-842d-49fc-aec2-e0dfa7f1eb0a
title: Método LocationDisp. CivicAddressReportFactory. StopListeningForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.StopListeningForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 36c58e9db0edb66735dcbd58c8e1968cfa8b1fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688643"
---
# <a name="locationdispcivicaddressreportfactorystoplisteningforreports-method"></a><span data-ttu-id="1dfd5-103">LocationDisp. CivicAddressReportFactory. StopListeningForReports, método</span><span class="sxs-lookup"><span data-stu-id="1dfd5-103">LocationDisp.CivicAddressReportFactory.StopListeningForReports method</span></span>

<span data-ttu-id="1dfd5-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="1dfd5-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1dfd5-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="1dfd5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1dfd5-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1dfd5-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="1dfd5-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="1dfd5-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="1dfd5-108">Detiene los eventos del informe de direcciones cívica.</span><span class="sxs-lookup"><span data-stu-id="1dfd5-108">Stops civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dfd5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dfd5-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.StopListeningForReports()
```



## <a name="parameters"></a><span data-ttu-id="1dfd5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1dfd5-110">Parameters</span></span>

<span data-ttu-id="1dfd5-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1dfd5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1dfd5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1dfd5-112">Return value</span></span>

<span data-ttu-id="1dfd5-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1dfd5-113">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="1dfd5-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1dfd5-114">Examples</span></span>

<span data-ttu-id="1dfd5-115">Para obtener un ejemplo de cómo usar este método, consulte [escucha de eventos de informe de direcciones cívica](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="1dfd5-115">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfd5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dfd5-116">Requirements</span></span>



| <span data-ttu-id="1dfd5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dfd5-117">Requirement</span></span> | <span data-ttu-id="1dfd5-118">Value</span><span class="sxs-lookup"><span data-stu-id="1dfd5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfd5-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dfd5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1dfd5-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1dfd5-120">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1dfd5-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dfd5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1dfd5-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1dfd5-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1dfd5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dfd5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dfd5-124"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dfd5-124"><dt>Locationapi.h</dt></span></span> </dl> |



 

