---
title: Enumeración SwarmStatus (Deliveryoptimization. h)
description: Define el estado de un archivo dentro del cliente de optimización de entrega.
ms.assetid: D40ABDD3-5573-4A8D-8608-4CB0F396CCAD
keywords:
- Enumeración SwarmStatus
topic_type:
- apiref
api_name:
- SwarmStatus
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3622f819679c2fd2b28d66e371a8b88e0a2d2f70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150832"
---
# <a name="swarmstatus-enumeration"></a><span data-ttu-id="3d5bb-104">Enumeración SwarmStatus</span><span class="sxs-lookup"><span data-stu-id="3d5bb-104">SwarmStatus enumeration</span></span>

<span data-ttu-id="3d5bb-105">Define el estado de un archivo dentro del cliente de optimización de entrega.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-105">Defines the status of a file within the delivery optimization client.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d5bb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d5bb-106">Syntax</span></span>


```C++
typedef enum _SwarmStatus { 
  SwarmStatus_Downloading  = 0,
  SwarmStatus_Complete     = 1,
  SwarmStatus_Caching      = 2,
  SwarmStatus_Paused       = 3
} SwarmStatus;
```



## <a name="constants"></a><span data-ttu-id="3d5bb-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="3d5bb-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3d5bb-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span><span class="sxs-lookup"><span data-stu-id="3d5bb-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span></span>
</dt> <dd>

<span data-ttu-id="3d5bb-109">El archivo se está descargando.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-109">The file is downloading.</span></span>

</dd> <dt>

<span data-ttu-id="3d5bb-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span><span class="sxs-lookup"><span data-stu-id="3d5bb-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span></span>
</dt> <dd>

<span data-ttu-id="3d5bb-111">Se completó la descarga del archivo.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-111">The file download is complete.</span></span>

</dd> <dt>

<span data-ttu-id="3d5bb-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span><span class="sxs-lookup"><span data-stu-id="3d5bb-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span></span>
</dt> <dd>

<span data-ttu-id="3d5bb-113">El archivo se está almacenando en caché.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-113">The file is being cached.</span></span>

</dd> <dt>

<span data-ttu-id="3d5bb-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span><span class="sxs-lookup"><span data-stu-id="3d5bb-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="3d5bb-115">La descarga del archivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-115">The file download is paused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d5bb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d5bb-116">Requirements</span></span>



| <span data-ttu-id="3d5bb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d5bb-117">Requirement</span></span> | <span data-ttu-id="3d5bb-118">Value</span><span class="sxs-lookup"><span data-stu-id="3d5bb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5bb-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d5bb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3d5bb-120">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d5bb-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d5bb-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d5bb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3d5bb-122">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3d5bb-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d5bb-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d5bb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d5bb-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d5bb-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





