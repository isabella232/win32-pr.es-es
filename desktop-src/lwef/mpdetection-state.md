---
title: Enumeración MPDETECTION_STATE (MpClient. h)
description: El estado de la amenaza detectada actualmente.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE enumeración características de entorno heredado de Windows
- PMPDETECTION_STATE el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490006"
---
# <a name="mpdetection_state-enumeration"></a><span data-ttu-id="fef4f-105">\_Enumeración de estado de MPDETECTION</span><span class="sxs-lookup"><span data-stu-id="fef4f-105">MPDETECTION\_STATE enumeration</span></span>

<span data-ttu-id="fef4f-106">El estado de la amenaza detectada actualmente.</span><span class="sxs-lookup"><span data-stu-id="fef4f-106">The state of the currently detected threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef4f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fef4f-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a><span data-ttu-id="fef4f-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="fef4f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fef4f-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**Estado de MPDETECTION \_ \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="fef4f-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION\_STATE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="fef4f-110">En un estado de error.</span><span class="sxs-lookup"><span data-stu-id="fef4f-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="fef4f-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**Estado de MPDETECTION \_ \_ activo**</span><span class="sxs-lookup"><span data-stu-id="fef4f-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION\_STATE\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="fef4f-112">Amenaza activa.</span><span class="sxs-lookup"><span data-stu-id="fef4f-112">Active threat.</span></span>

</dd> <dt>

<span data-ttu-id="fef4f-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**Estado de MPDETECTION \_ \_ finalizado**</span><span class="sxs-lookup"><span data-stu-id="fef4f-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="fef4f-114">Pendiente 24 horas hasta que se desactive el movimiento.</span><span class="sxs-lookup"><span data-stu-id="fef4f-114">Pending 24 hours to a move to cleared.</span></span>

</dd> <dt>

<span data-ttu-id="fef4f-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**\_ \_ acciones adicionales de estado de MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="fef4f-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION\_STATE\_ADDITIONAL\_ACTIONS**</span></span>
</dt> <dd>

<span data-ttu-id="fef4f-116">Acciones adicionales necesarias.</span><span class="sxs-lookup"><span data-stu-id="fef4f-116">Additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="fef4f-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**\_error de estado de MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="fef4f-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION\_STATE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="fef4f-118">Error de corrección no crítico.</span><span class="sxs-lookup"><span data-stu-id="fef4f-118">Non-critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="fef4f-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**Estado de MPDETECTION de \_ \_ \_ error crítico**</span><span class="sxs-lookup"><span data-stu-id="fef4f-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION\_STATE\_CRITICALLY\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="fef4f-120">Error crítico en la corrección.</span><span class="sxs-lookup"><span data-stu-id="fef4f-120">Critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="fef4f-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**Estado de MPDETECTION \_ \_ desactivado**</span><span class="sxs-lookup"><span data-stu-id="fef4f-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**MPDETECTION\_STATE\_CLEARED**</span></span>
</dt> <dd>

<span data-ttu-id="fef4f-122">La amenaza no se muestra en la consulta de estado, solo en el historial.</span><span class="sxs-lookup"><span data-stu-id="fef4f-122">Threat does not show up in the state query, only in history.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fef4f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fef4f-123">Requirements</span></span>



| <span data-ttu-id="fef4f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fef4f-124">Requirement</span></span> | <span data-ttu-id="fef4f-125">Value</span><span class="sxs-lookup"><span data-stu-id="fef4f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fef4f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fef4f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fef4f-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fef4f-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fef4f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fef4f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fef4f-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fef4f-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fef4f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fef4f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fef4f-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fef4f-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





