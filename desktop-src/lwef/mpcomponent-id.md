---
title: Enumeración MPCOMPONENT_ID (MpClient. h)
description: Componentes posibles para el administrador de protección contra malware de.
ms.assetid: 014B400A-880B-419D-9F50-F3354CE945D9
keywords:
- MPCOMPONENT_ID enumeración características de entorno heredado de Windows
- PMPCOMPONENT_ID el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_ID
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196eebc5a3bee4968878c376cd7358724c9c55cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150146"
---
# <a name="mpcomponent_id-enumeration"></a><span data-ttu-id="1cf36-105">\_Enumeración de MPCOMPONENT ID</span><span class="sxs-lookup"><span data-stu-id="1cf36-105">MPCOMPONENT\_ID enumeration</span></span>

<span data-ttu-id="1cf36-106">Componentes posibles para el administrador de protección contra malware de.</span><span class="sxs-lookup"><span data-stu-id="1cf36-106">Possible components for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf36-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cf36-107">Syntax</span></span>


```C++
typedef enum tagMPCOMPONENT_ID { 
  MPCOMPONENT_AS_SIGNATURE         = 0,
  MPCOMPONENT_AV_SIGNATURE         = 1,
  MPCOMPONENT_REALTIME_MONITOR     = 2,
  MPCOMPONENT_ONACCESS_PROTECTION  = 3,
  MPCOMPONENT_IOAV_PROTECTION      = 4,
  MPCOMPONENT_BEHAVIOR_MONITOR     = 5,
  MPCOMPONENT_AUTO_SCAN            = 6,
  MPCOMPONENT_AUTO_SIGUPDATE       = 7,
  MPCOMPONENT_IPC                  = 8,
  MPCOMPONENT_NIS                  = 9,
  MPCOMPONENT_ELAM                 = 10,
  MPCOMPONENT_MAXVALUE             = 10
} MPCOMPONENT_ID, *PMPCOMPONENT_ID;
```



## <a name="constants"></a><span data-ttu-id="1cf36-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="1cf36-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1cf36-109"><span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**MPCOMPONENT \_ como \_ firma**</span><span class="sxs-lookup"><span data-stu-id="1cf36-109"><span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**MPCOMPONENT\_AS\_SIGNATURE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-110"><span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**\_firma de AV MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="1cf36-110"><span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**MPCOMPONENT\_AV\_SIGNATURE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-111"><span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**MONITOR de MPCOMPONENT en \_ tiempo real \_**</span><span class="sxs-lookup"><span data-stu-id="1cf36-111"><span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**MPCOMPONENT\_REALTIME\_MONITOR**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-112"><span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**protección de MPCOMPONENT de \_ acceso \_**</span><span class="sxs-lookup"><span data-stu-id="1cf36-112"><span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**MPCOMPONENT\_ONACCESS\_PROTECTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-113"><span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**\_protección de IOAV de MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="1cf36-113"><span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**MPCOMPONENT\_IOAV\_PROTECTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-114"><span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**\_monitor de comportamiento de MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="1cf36-114"><span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**MPCOMPONENT\_BEHAVIOR\_MONITOR**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-115"><span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**\_examen automático de MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="1cf36-115"><span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**MPCOMPONENT\_AUTO\_SCAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-116"><span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**\_SIGUPDATE MPCOMPONENT auto \_**</span><span class="sxs-lookup"><span data-stu-id="1cf36-116"><span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**MPCOMPONENT\_AUTO\_SIGUPDATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-117"><span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**\_IPC MPCOMPONENT**</span><span class="sxs-lookup"><span data-stu-id="1cf36-117"><span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**MPCOMPONENT\_IPC**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-118"><span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**MPCOMPONENT \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="1cf36-118"><span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**MPCOMPONENT\_NIS**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-119"><span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**MPCOMPONENT \_ Elam**</span><span class="sxs-lookup"><span data-stu-id="1cf36-119"><span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**MPCOMPONENT\_ELAM**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1cf36-120"><span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**MPCOMPONENT \_ MAXVALUE**</span><span class="sxs-lookup"><span data-stu-id="1cf36-120"><span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**MPCOMPONENT\_MAXVALUE**</span></span>
<span data-ttu-id="1cf36-121"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1cf36-121"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1cf36-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cf36-122">Requirements</span></span>



| <span data-ttu-id="1cf36-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cf36-123">Requirement</span></span> | <span data-ttu-id="1cf36-124">Value</span><span class="sxs-lookup"><span data-stu-id="1cf36-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf36-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cf36-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf36-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cf36-126">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1cf36-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cf36-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf36-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cf36-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cf36-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cf36-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cf36-130"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cf36-130"><dt>MpClient.h</dt></span></span> </dl> |



 

 





