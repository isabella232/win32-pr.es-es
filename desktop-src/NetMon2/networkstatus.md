---
description: La estructura NETWORKSTATUS describe el estado actual del NPP.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Estructura NETWORKSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546995"
---
# <a name="networkstatus-structure"></a><span data-ttu-id="c5ac5-103">Estructura NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="c5ac5-103">NETWORKSTATUS structure</span></span>

<span data-ttu-id="c5ac5-104">La estructura **NETWORKSTATUS** describe el estado actual del NPP.</span><span class="sxs-lookup"><span data-stu-id="c5ac5-104">The **NETWORKSTATUS** structure describes the current status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ac5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5ac5-105">Syntax</span></span>


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a><span data-ttu-id="c5ac5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c5ac5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5ac5-107">**State**</span><span class="sxs-lookup"><span data-stu-id="c5ac5-107">**State**</span></span>
</dt> <dd>

<span data-ttu-id="c5ac5-108">Indica el estado actual del NPP.</span><span class="sxs-lookup"><span data-stu-id="c5ac5-108">Indicates the current state of the NPP.</span></span>



| <span data-ttu-id="c5ac5-109">Value</span><span class="sxs-lookup"><span data-stu-id="c5ac5-109">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="c5ac5-110">Significado</span><span class="sxs-lookup"><span data-stu-id="c5ac5-110">Meaning</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <span data-ttu-id="c5ac5-111"><dt>**NETWORKSTATUS \_ estado \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ac5-111"><dt>**NETWORKSTATUS\_STATE\_VOID**</dt></span></span> </dl>                | <span data-ttu-id="c5ac5-112">NPP no está conectado o está conectado y la captura no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="c5ac5-112">The NPP is not connected, or it is connected and the capture is not started.</span></span><br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <span data-ttu-id="c5ac5-113"><dt>**\_captura de estado de NETWORKSTATUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ac5-113"><dt>**NETWORKSTATUS\_STATE\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="c5ac5-114">NPP está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="c5ac5-114">The NPP is capturing data.</span></span><br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <span data-ttu-id="c5ac5-115"><dt>**Estado de NETWORKSTATUS en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ac5-115"><dt>**NETWORKSTATUS\_STATE\_PAUSED**</dt></span></span> </dl>          | <span data-ttu-id="c5ac5-116">El NPP se ha pausado durante la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="c5ac5-116">The NPP has paused while capturing data.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="c5ac5-117">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="c5ac5-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="c5ac5-118">Marcas que describen el estado actual del NPP.</span><span class="sxs-lookup"><span data-stu-id="c5ac5-118">Flags that describe the current state of the NPP.</span></span>



| <span data-ttu-id="c5ac5-119">Value</span><span class="sxs-lookup"><span data-stu-id="c5ac5-119">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="c5ac5-120">Significado</span><span class="sxs-lookup"><span data-stu-id="c5ac5-120">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <span data-ttu-id="c5ac5-121"><dt>**\_desencadenador de marcas de NETWORKSTATUS \_ \_ pendiente**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ac5-121"><dt>**NETWORKSTATUS\_FLAGS\_TRIGGER\_PENDING**</dt></span></span> </dl> | <span data-ttu-id="c5ac5-122">Hay un desencadenador pendiente para el NPP.</span><span class="sxs-lookup"><span data-stu-id="c5ac5-122">There is a trigger pending for the NPP.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5ac5-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5ac5-123">Remarks</span></span>

<span data-ttu-id="c5ac5-124">Al utilizar esta estructura, debe asignar la memoria de la estructura antes de que se pueda utilizar y liberar la memoria cuando la estructura ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="c5ac5-124">When using this structure, you must allocate the memory for the structure before it can be used and free the memory when the structure is no longer needed.</span></span>

<span data-ttu-id="c5ac5-125">En la lista vea también en la parte inferior de este tema se enumeran todos los métodos que utilizan esta estructura.</span><span class="sxs-lookup"><span data-stu-id="c5ac5-125">The See Also list at the bottom of this topic lists all the methods that use this structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ac5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5ac5-126">Requirements</span></span>



| <span data-ttu-id="c5ac5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ac5-127">Requirement</span></span> | <span data-ttu-id="c5ac5-128">Value</span><span class="sxs-lookup"><span data-stu-id="c5ac5-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ac5-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5ac5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ac5-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c5ac5-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c5ac5-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5ac5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ac5-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c5ac5-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c5ac5-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5ac5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ac5-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ac5-134"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ac5-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5ac5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ac5-136">IDelaydC:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="c5ac5-136">IDelaydC::QueryStatus</span></span>](idelaydc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="c5ac5-137">IESP:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="c5ac5-137">IESP::QueryStatus</span></span>](iesp-querystatus.md)
</dt> <dt>

[<span data-ttu-id="c5ac5-138">IRTC:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="c5ac5-138">IRTC::QueryStatus</span></span>](irtc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="c5ac5-139">IStas:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="c5ac5-139">IStats::QueryStatus</span></span>](istats-querystatus.md)
</dt> </dl>

 

 




