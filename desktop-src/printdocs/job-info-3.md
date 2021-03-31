---
description: La \_ estructura Job info \_ 3 se usa para vincular un conjunto de trabajos de impresión.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Estructura de JOB_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279024"
---
# <a name="job_info_3-structure"></a><span data-ttu-id="431b6-103">Estructura de información de trabajo \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="431b6-103">JOB\_INFO\_3 structure</span></span>

<span data-ttu-id="431b6-104">La estructura **Job \_ info \_ 3** se usa para vincular un conjunto de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="431b6-104">The **JOB\_INFO\_3** structure is used to link together a set of print jobs.</span></span>

## <a name="syntax"></a><span data-ttu-id="431b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="431b6-105">Syntax</span></span>


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a><span data-ttu-id="431b6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="431b6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="431b6-107">**JobId**</span><span class="sxs-lookup"><span data-stu-id="431b6-107">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="431b6-108">Identificador del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="431b6-108">The print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="431b6-109">**NextJobId**</span><span class="sxs-lookup"><span data-stu-id="431b6-109">**NextJobId**</span></span>
</dt> <dd>

<span data-ttu-id="431b6-110">Identificador del trabajo de impresión para el siguiente trabajo de impresión en el conjunto vinculado de trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="431b6-110">The print job identifier for the next print job in the linked set of print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="431b6-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="431b6-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="431b6-112">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="431b6-112">This value is reserved for future use.</span></span> <span data-ttu-id="431b6-113">Debe establecerlo en cero.</span><span class="sxs-lookup"><span data-stu-id="431b6-113">You must set it to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="431b6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431b6-114">Requirements</span></span>



| <span data-ttu-id="431b6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="431b6-115">Requirement</span></span> | <span data-ttu-id="431b6-116">Value</span><span class="sxs-lookup"><span data-stu-id="431b6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="431b6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="431b6-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="431b6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="431b6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="431b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="431b6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="431b6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="431b6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="431b6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="431b6-122"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="431b6-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431b6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="431b6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431b6-124">Impresión</span><span class="sxs-lookup"><span data-stu-id="431b6-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="431b6-125">Estructuras de API del administrador de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="431b6-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="431b6-126">**EnumJobs**</span><span class="sxs-lookup"><span data-stu-id="431b6-126">**EnumJobs**</span></span>](enumjobs.md)
</dt> <dt>

[<span data-ttu-id="431b6-127">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="431b6-127">**GetJob**</span></span>](getjob.md)
</dt> <dt>

[<span data-ttu-id="431b6-128">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="431b6-128">**SetJob**</span></span>](setjob.md)
</dt> </dl>

 

 




