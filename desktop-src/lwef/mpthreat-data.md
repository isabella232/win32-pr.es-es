---
title: MPTHREAT_DATA estructura (MpClient. h)
description: Datos de notificación pasados debido a la detección de amenazas o a la modificación.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714643"
---
# <a name="mpthreat_data-structure"></a><span data-ttu-id="07b09-105">\_Estructura de datos MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="07b09-105">MPTHREAT\_DATA structure</span></span>

<span data-ttu-id="07b09-106">Datos de notificación pasados debido a la detección de amenazas o a la modificación.</span><span class="sxs-lookup"><span data-stu-id="07b09-106">Notification data passed due to threat detection or modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b09-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07b09-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a><span data-ttu-id="07b09-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="07b09-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="07b09-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="07b09-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="07b09-110">Tipo: **\_ ID. de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="07b09-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="07b09-111">Identificador de amenaza.</span><span class="sxs-lookup"><span data-stu-id="07b09-111">Threat identifier.</span></span> <span data-ttu-id="07b09-112">El bit superior se establece para identificar las amenazas relacionadas con el antivirus.</span><span class="sxs-lookup"><span data-stu-id="07b09-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="07b09-113">**dwSessionID**</span><span class="sxs-lookup"><span data-stu-id="07b09-113">**dwSessionID**</span></span>
</dt> <dd>

<span data-ttu-id="07b09-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="07b09-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="07b09-115">Sesión asociada a la amenaza.</span><span class="sxs-lookup"><span data-stu-id="07b09-115">Session associated with the threat.</span></span> <span data-ttu-id="07b09-116">Establézcalo en-1 si no hay disponible ninguna información específica de la sesión.</span><span class="sxs-lookup"><span data-stu-id="07b09-116">Set to -1 if no session specific information is available.</span></span>

</dd> <dt>

<span data-ttu-id="07b09-117">**ThreatAction**</span><span class="sxs-lookup"><span data-stu-id="07b09-117">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="07b09-118">Tipo: **[ **\_ acción MPTHREAT**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="07b09-118">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="07b09-119">Se intentó una acción de amenaza para los eventos de **\_ \_ \_** / **\_ \_ \_ error al limpiar** la amenaza de MPNOTIFY correctamente MPNOTIFY.</span><span class="sxs-lookup"><span data-stu-id="07b09-119">Threat action tried for the **MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**/**MPNOTIFY\_THREAT\_CLEAN\_FAILED** events.</span></span>

</dd> <dt>

<span data-ttu-id="07b09-120">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="07b09-120">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="07b09-121">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="07b09-121">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="07b09-122">Estado adicional o acciones asociadas a la acción realizada.</span><span class="sxs-lookup"><span data-stu-id="07b09-122">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="07b09-123">Se trata de una combinación de marcas de bits de la [**\_ marca MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="07b09-123">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07b09-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b09-124">Requirements</span></span>



| <span data-ttu-id="07b09-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b09-125">Requirement</span></span> | <span data-ttu-id="07b09-126">Value</span><span class="sxs-lookup"><span data-stu-id="07b09-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07b09-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07b09-127">Minimum supported client</span></span><br/> | <span data-ttu-id="07b09-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="07b09-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="07b09-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07b09-129">Minimum supported server</span></span><br/> | <span data-ttu-id="07b09-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="07b09-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07b09-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07b09-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="07b09-132"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="07b09-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b09-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="07b09-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b09-134">**\_marca MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="07b09-134">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="07b09-135">**\_acción MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="07b09-135">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





