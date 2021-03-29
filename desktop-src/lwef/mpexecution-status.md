---
title: Enumeración MPEXECUTION_STATUS (MpClient. h)
description: Posible estado de ejecución de la amenaza.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS enumeración características de entorno heredado de Windows
- PMPEXECUTION_STATUS el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905142"
---
# <a name="mpexecution_status-enumeration"></a><span data-ttu-id="a7b1a-105">\_Enumeración de estado de MPEXECUTION</span><span class="sxs-lookup"><span data-stu-id="a7b1a-105">MPEXECUTION\_STATUS enumeration</span></span>

<span data-ttu-id="a7b1a-106">Posible estado de ejecución de la amenaza.</span><span class="sxs-lookup"><span data-stu-id="a7b1a-106">Possible threat execution status.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b1a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7b1a-107">Syntax</span></span>


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a><span data-ttu-id="a7b1a-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a7b1a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a7b1a-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**Estado de ejecución del módulo de administración \_ \_ \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="a7b1a-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP\_EXECUTION\_STATUS\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="a7b1a-110">No se conoce el estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a7b1a-110">Execution status is not known.</span></span>

</dd> <dt>

<span data-ttu-id="a7b1a-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**Estado de ejecución del módulo de administración \_ \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="a7b1a-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP\_EXECUTION\_STATUS\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="a7b1a-112">No se ha bloqueado la ejecución mediante el filtro Mini.</span><span class="sxs-lookup"><span data-stu-id="a7b1a-112">Blocked from execution by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="a7b1a-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**Estado de ejecución de MP \_ \_ \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="a7b1a-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**MP\_EXECUTION\_STATUS\_ALLOWED**</span></span>
</dt> <dd>

<span data-ttu-id="a7b1a-114">Se permite que se ejecute mediante un filtro Mini.</span><span class="sxs-lookup"><span data-stu-id="a7b1a-114">Allowed to execute by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="a7b1a-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**Estado de ejecución del módulo de administración en \_ \_ \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="a7b1a-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**MP\_EXECUTION\_STATUS\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="a7b1a-116">Se está ejecutando una amenaza.</span><span class="sxs-lookup"><span data-stu-id="a7b1a-116">Threat is executing.</span></span>

</dd> <dt>

<span data-ttu-id="a7b1a-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**Estado de ejecución del módulo de administración \_ \_ no en \_ \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="a7b1a-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP\_EXECUTION\_STATUS\_NOT\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="a7b1a-118">La amenaza no se está ejecutando y solo está disponible en el motor durante la corrección.</span><span class="sxs-lookup"><span data-stu-id="a7b1a-118">Threat is not executing, and is only available from the engine during remediation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7b1a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7b1a-119">Requirements</span></span>



| <span data-ttu-id="a7b1a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7b1a-120">Requirement</span></span> | <span data-ttu-id="a7b1a-121">Value</span><span class="sxs-lookup"><span data-stu-id="a7b1a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b1a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7b1a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b1a-123">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7b1a-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a7b1a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7b1a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b1a-125">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7b1a-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7b1a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7b1a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b1a-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b1a-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





