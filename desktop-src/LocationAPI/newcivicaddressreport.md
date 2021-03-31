---
description: Se produce cuando se genera un nuevo informe de dirección cívica.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Evento NewCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: fa786ecee4ce4223cdb7ec0c8400c5c11bf6e192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913509"
---
# <a name="newcivicaddressreport-event"></a><span data-ttu-id="bedbf-103">Evento NewCivicAddressReport</span><span class="sxs-lookup"><span data-stu-id="bedbf-103">NewCivicAddressReport event</span></span>

<span data-ttu-id="bedbf-104">\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="bedbf-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bedbf-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="bedbf-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="bedbf-106">En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bedbf-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="bedbf-107">Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="bedbf-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="bedbf-108">Se produce cuando se genera un nuevo informe de dirección cívica.</span><span class="sxs-lookup"><span data-stu-id="bedbf-108">Occurs when a new civic address report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="bedbf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bedbf-109">Syntax</span></span>


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="bedbf-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bedbf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bedbf-111">*newReport*</span><span class="sxs-lookup"><span data-stu-id="bedbf-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="bedbf-112">El nuevo objeto [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) .</span><span class="sxs-lookup"><span data-stu-id="bedbf-112">The new [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bedbf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bedbf-113">Return value</span></span>

<span data-ttu-id="bedbf-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="bedbf-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="bedbf-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bedbf-115">Examples</span></span>

<span data-ttu-id="bedbf-116">Para obtener un ejemplo de cómo usar este evento, consulte [escucha de eventos de informe de direcciones cívica](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="bedbf-116">For an example of how to use this event, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="bedbf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bedbf-117">Requirements</span></span>



| <span data-ttu-id="bedbf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bedbf-118">Requirement</span></span> | <span data-ttu-id="bedbf-119">Value</span><span class="sxs-lookup"><span data-stu-id="bedbf-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="bedbf-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bedbf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bedbf-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bedbf-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bedbf-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bedbf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bedbf-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bedbf-123">None supported</span></span><br/>                  |



 

