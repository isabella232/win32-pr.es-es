---
title: Enumeración DODownloadCostPolicy
description: Especifica el identificador de las opciones de directivas de costos asociadas a la propiedad **DODownloadProperty_CostPolicy** .
keywords:
- Enumeración DODownloadCostPolicy, DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421983"
---
# <a name="dodownloadcostpolicy-enumeration"></a><span data-ttu-id="423e5-104">Enumeración DODownloadCostPolicy</span><span class="sxs-lookup"><span data-stu-id="423e5-104">DODownloadCostPolicy enumeration</span></span>

<span data-ttu-id="423e5-105">La enumeración **DODownloadCostPolicy** especifica el identificador de las opciones de directivas de costos asociadas a la propiedad **DODownloadProperty_CostPolicy** .</span><span class="sxs-lookup"><span data-stu-id="423e5-105">The **DODownloadCostPolicy** enumeration specifies the ID of cost policies options associated with the **DODownloadProperty_CostPolicy** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="423e5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="423e5-106">Syntax</span></span>

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a><span data-ttu-id="423e5-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="423e5-107">Constants</span></span>

| <span data-ttu-id="423e5-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="423e5-108">Requirement</span></span> | <span data-ttu-id="423e5-109">Value</span><span class="sxs-lookup"><span data-stu-id="423e5-109">Value</span></span> |
|-|-|
| <span data-ttu-id="423e5-110">DODownloadCostPolicy_Always</span><span class="sxs-lookup"><span data-stu-id="423e5-110">DODownloadCostPolicy_Always</span></span> | <span data-ttu-id="423e5-111">La descarga se ejecuta independientemente del costo.</span><span class="sxs-lookup"><span data-stu-id="423e5-111">Download runs regardless of the cost.</span></span> |
| <span data-ttu-id="423e5-112">DODownloadCostPolicy_Unrestricted</span><span class="sxs-lookup"><span data-stu-id="423e5-112">DODownloadCostPolicy_Unrestricted</span></span> | <span data-ttu-id="423e5-113">Descarga se ejecuta a menos que imponga costos o límites de tráfico.</span><span class="sxs-lookup"><span data-stu-id="423e5-113">Download runs unless imposes costs or traffic limits.</span></span> |
| <span data-ttu-id="423e5-114">DODownloadCostPolicy_Standard</span><span class="sxs-lookup"><span data-stu-id="423e5-114">DODownloadCostPolicy_Standard</span></span> | <span data-ttu-id="423e5-115">Descarga se ejecuta a menos que no esté sujeto a un recargo ni a un agotamiento cercano.</span><span class="sxs-lookup"><span data-stu-id="423e5-115">Download runs unless neither subject to a surcharge nor near exhaustion.</span></span> |
| <span data-ttu-id="423e5-116">DODownloadCostPolicy_NoRoaming</span><span class="sxs-lookup"><span data-stu-id="423e5-116">DODownloadCostPolicy_NoRoaming</span></span> | <span data-ttu-id="423e5-117">La descarga se ejecuta a menos que la conectividad esté sujeta a suplementos móviles.</span><span class="sxs-lookup"><span data-stu-id="423e5-117">Download runs unless that connectivity is subject to roaming surcharges.</span></span> |
| <span data-ttu-id="423e5-118">DODownloadCostPolicy_NoSurcharge</span><span class="sxs-lookup"><span data-stu-id="423e5-118">DODownloadCostPolicy_NoSurcharge</span></span> | <span data-ttu-id="423e5-119">Descarga se ejecuta a menos que esté sujeto a un suplemento.</span><span class="sxs-lookup"><span data-stu-id="423e5-119">Download runs unless subject to a surcharge.</span></span> |
| <span data-ttu-id="423e5-120">DODownloadCostPolicy_NoCellular</span><span class="sxs-lookup"><span data-stu-id="423e5-120">DODownloadCostPolicy_NoCellular</span></span> | <span data-ttu-id="423e5-121">Descarga se ejecuta a menos que la red sea móvil.</span><span class="sxs-lookup"><span data-stu-id="423e5-121">Download runs unless network is on cellular.</span></span> |

## <a name="requirements"></a><span data-ttu-id="423e5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="423e5-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="423e5-123">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="423e5-123">**Minimum supported client**</span></span> | <span data-ttu-id="423e5-124">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="423e5-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="423e5-125">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="423e5-125">**Minimum supported server**</span></span> | <span data-ttu-id="423e5-126">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="423e5-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="423e5-127">**Header**</span><span class="sxs-lookup"><span data-stu-id="423e5-127">**Header**</span></span> | <span data-ttu-id="423e5-128">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="423e5-128">DeliveryOptimizationDownloadTypes.h</span></span> |
