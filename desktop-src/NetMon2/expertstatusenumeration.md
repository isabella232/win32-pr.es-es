---
description: La enumeración EXPERTSTATUSENUMERATION contiene valores de estado. Lo usa el miembro status de la estructura EXPERTSTATUS y el parámetro status en ExpertIndicateStatus.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Enumeración EXPERTSTATUSENUMERATION (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666294"
---
# <a name="expertstatusenumeration-enumeration"></a><span data-ttu-id="5e12e-104">Enumeración EXPERTSTATUSENUMERATION</span><span class="sxs-lookup"><span data-stu-id="5e12e-104">EXPERTSTATUSENUMERATION enumeration</span></span>

<span data-ttu-id="5e12e-105">La enumeración **EXPERTSTATUSENUMERATION** contiene valores de estado.</span><span class="sxs-lookup"><span data-stu-id="5e12e-105">The **EXPERTSTATUSENUMERATION** enumeration contains status values.</span></span> <span data-ttu-id="5e12e-106">Lo usa el miembro **status** de la estructura [EXPERTSTATUS](expertstatus.md) y el parámetro *status* en [ExpertIndicateStatus](expertindicatestatus.md).</span><span class="sxs-lookup"><span data-stu-id="5e12e-106">It is used by the **Status** member of [EXPERTSTATUS](expertstatus.md) structure and the *Status* parameter in [ExpertIndicateStatus](expertindicatestatus.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e12e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e12e-107">Syntax</span></span>


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a><span data-ttu-id="5e12e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5e12e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5e12e-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ INactivo**</span><span class="sxs-lookup"><span data-stu-id="5e12e-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="5e12e-110">El experto nunca comenzó.</span><span class="sxs-lookup"><span data-stu-id="5e12e-110">The expert never started.</span></span>

</dd> <dt>

<span data-ttu-id="5e12e-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**Inicio de EXPERTSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="5e12e-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS\_STARTING**</span></span>
</dt> <dd>

<span data-ttu-id="5e12e-112">Se está iniciando el experto.</span><span class="sxs-lookup"><span data-stu-id="5e12e-112">The expert is starting.</span></span>

</dd> <dt>

<span data-ttu-id="5e12e-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS en \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="5e12e-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="5e12e-114">El experto se ejecuta con normalidad.</span><span class="sxs-lookup"><span data-stu-id="5e12e-114">The expert is running normally.</span></span>

</dd> <dt>

<span data-ttu-id="5e12e-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**problema de EXPERTSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="5e12e-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**EXPERTSTATUS\_PROBLEM**</span></span>
</dt> <dd>

<span data-ttu-id="5e12e-116">Un problema especificado en el *subestado* detuvo el experto.</span><span class="sxs-lookup"><span data-stu-id="5e12e-116">A problem specified in *SubStatus* stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="5e12e-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="5e12e-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="5e12e-118">Monitor de red detuvo el experto.</span><span class="sxs-lookup"><span data-stu-id="5e12e-118">Network Monitor stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="5e12e-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ completado**</span><span class="sxs-lookup"><span data-stu-id="5e12e-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS\_DONE**</span></span>
</dt> <dd>

<span data-ttu-id="5e12e-120">El experto ha finalizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e12e-120">The expert finished successfully.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e12e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e12e-121">Requirements</span></span>



| <span data-ttu-id="5e12e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e12e-122">Requirement</span></span> | <span data-ttu-id="5e12e-123">Value</span><span class="sxs-lookup"><span data-stu-id="5e12e-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5e12e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e12e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5e12e-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5e12e-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5e12e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e12e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5e12e-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5e12e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5e12e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e12e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e12e-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e12e-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




