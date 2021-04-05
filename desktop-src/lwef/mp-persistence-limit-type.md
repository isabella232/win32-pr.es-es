---
title: Enumeración MP_PERSISTENCE_LIMIT_TYPE (MpClient. h)
description: Tipo de límite de persistencia.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE enumeración características de entorno heredado de Windows
- PMP_PERSISTENCE_LIMIT_TYPE el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb52bc6ee630590ca189b88c1fdde5a30e17747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079684"
---
# <a name="mp_persistence_limit_type-enumeration"></a><span data-ttu-id="c0535-105">\_ \_ Enumeración de tipo de límite de persistencia de MP \_</span><span class="sxs-lookup"><span data-stu-id="c0535-105">MP\_PERSISTENCE\_LIMIT\_TYPE enumeration</span></span>

<span data-ttu-id="c0535-106">Tipo de límite de persistencia.</span><span class="sxs-lookup"><span data-stu-id="c0535-106">Persistence limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0535-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0535-107">Syntax</span></span>


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="c0535-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="c0535-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c0535-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**persistencia de MP \_ \_ desconocida**</span><span class="sxs-lookup"><span data-stu-id="c0535-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP\_PERSISTENCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="c0535-110">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="c0535-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="c0535-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**persistencia de MP \_ \_ sin \_ límite**</span><span class="sxs-lookup"><span data-stu-id="c0535-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP\_PERSISTENCE\_NO\_LIMIT**</span></span>
</dt> <dd>

<span data-ttu-id="c0535-112">Ilimitado.</span><span class="sxs-lookup"><span data-stu-id="c0535-112">No limit.</span></span>

</dd> <dt>

<span data-ttu-id="c0535-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**\_duración de persistencia de MP \_**</span><span class="sxs-lookup"><span data-stu-id="c0535-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP\_PERSISTENCE\_DURATION**</span></span>
</dt> <dd>

<span data-ttu-id="c0535-114">Duración.</span><span class="sxs-lookup"><span data-stu-id="c0535-114">Duration.</span></span>

</dd> <dt>

<span data-ttu-id="c0535-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**\_versión de \_ VDM de persistencia de MP \_**</span><span class="sxs-lookup"><span data-stu-id="c0535-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP\_PERSISTENCE\_VDM\_VERSION**</span></span>
</dt> <dd>

<span data-ttu-id="c0535-116">Versión de VDM.</span><span class="sxs-lookup"><span data-stu-id="c0535-116">VDM version.</span></span>

</dd> <dt>

<span data-ttu-id="c0535-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**marca de tiempo de persistencia de MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c0535-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP\_PERSISTENCE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="c0535-118">Timestamp.</span><span class="sxs-lookup"><span data-stu-id="c0535-118">Timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="c0535-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**persistencia de MP \_ \_ forzada**</span><span class="sxs-lookup"><span data-stu-id="c0535-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP\_PERSISTENCE\_FORCED**</span></span>
</dt> <dd>

<span data-ttu-id="c0535-120">Obliga.</span><span class="sxs-lookup"><span data-stu-id="c0535-120">Forced.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0535-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0535-121">Requirements</span></span>



| <span data-ttu-id="c0535-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0535-122">Requirement</span></span> | <span data-ttu-id="c0535-123">Value</span><span class="sxs-lookup"><span data-stu-id="c0535-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0535-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0535-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c0535-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0535-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c0535-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0535-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c0535-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0535-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0535-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0535-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0535-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0535-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





