---
title: Enumeración MPTHREAT_ACTION (MpClient. h)
description: Posibles acciones de amenaza.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- MPTHREAT_ACTION enumeración características de entorno heredado de Windows
- PMPTHREAT_ACTION el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0377517af590072b797a57c051ad062842ea9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150234"
---
# <a name="mpthreat_action-enumeration"></a><span data-ttu-id="fd4ae-105">\_Enumeración de acciones de MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="fd4ae-105">MPTHREAT\_ACTION enumeration</span></span>

<span data-ttu-id="fd4ae-106">Posibles acciones de amenaza.</span><span class="sxs-lookup"><span data-stu-id="fd4ae-106">Possible threat actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd4ae-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd4ae-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a><span data-ttu-id="fd4ae-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="fd4ae-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd4ae-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**acción de amenaza de MP \_ \_ \_ desconocida**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP\_THREAT\_ACTION\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="fd4ae-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**acción de amenaza de MP \_ \_ \_ limpia**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP\_THREAT\_ACTION\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="fd4ae-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**\_cuarentena de \_ acción de amenazas MP \_**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**MP\_THREAT\_ACTION\_QUARANTINE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="fd4ae-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**\_eliminación de \_ acción de amenaza de MP \_**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP\_THREAT\_ACTION\_REMOVE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="fd4ae-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**\_ \_ permitir acción de amenaza de MP \_**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP\_THREAT\_ACTION\_ALLOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="fd4ae-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**acción de amenaza del módulo de administración \_ \_ \_ USERDEFINED**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**MP\_THREAT\_ACTION\_USERDEFINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="fd4ae-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**acción de amenaza de MP no \_ \_ \_ Action**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP\_THREAT\_ACTION\_NOACTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="fd4ae-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**\_bloque de \_ acción de amenazas MP \_**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP\_THREAT\_ACTION\_BLOCK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="fd4ae-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**\_ \_ valor máximo de acción de amenaza de \_ MP \_**</span><span class="sxs-lookup"><span data-stu-id="fd4ae-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**MP\_THREAT\_ACTION\_MAX\_VALUE**</span></span>
<span data-ttu-id="fd4ae-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fd4ae-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="fd4ae-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd4ae-119">Requirements</span></span>



| <span data-ttu-id="fd4ae-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd4ae-120">Requirement</span></span> | <span data-ttu-id="fd4ae-121">Value</span><span class="sxs-lookup"><span data-stu-id="fd4ae-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd4ae-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd4ae-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fd4ae-123">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd4ae-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fd4ae-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd4ae-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fd4ae-125">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd4ae-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd4ae-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd4ae-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd4ae-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd4ae-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





