---
title: Enumeración MP_REMOVAL_REASON (MpClient. h)
description: Motivo de eliminación de la firma de FastPath.
ms.assetid: A09B4903-E53C-4DA1-BD0B-6DE0124FCAB3
keywords:
- MP_REMOVAL_REASON enumeración características de entorno heredado de Windows
- PMP_REMOVAL_REASON el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MP_REMOVAL_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ce70f46bd95d4183343990b40594326ed5d3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803541"
---
# <a name="mp_removal_reason-enumeration"></a><span data-ttu-id="e0430-105">\_Enumeración del motivo de eliminación de MP \_</span><span class="sxs-lookup"><span data-stu-id="e0430-105">MP\_REMOVAL\_REASON enumeration</span></span>

<span data-ttu-id="e0430-106">Motivo de eliminación de la firma de FastPath.</span><span class="sxs-lookup"><span data-stu-id="e0430-106">FastPath signature removal reason.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0430-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0430-107">Syntax</span></span>


```C++
typedef enum tagMP_REMOVAL_REASON { 
  MP_REMOVAL_UNKNOWN    = 0,
  MP_REMOVAL_MANUAL     = 1,
  MP_REMOVAL_AUTOMATIC  = 2
} MP_REMOVAL_REASON, *PMP_REMOVAL_REASON;
```



## <a name="constants"></a><span data-ttu-id="e0430-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e0430-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e0430-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**eliminación de MP \_ \_ desconocida**</span><span class="sxs-lookup"><span data-stu-id="e0430-109"><span id="MP_REMOVAL_UNKNOWN"></span><span id="mp_removal_unknown"></span>**MP\_REMOVAL\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="e0430-110">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="e0430-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="e0430-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**\_manual de eliminación de MP \_**</span><span class="sxs-lookup"><span data-stu-id="e0430-111"><span id="MP_REMOVAL_MANUAL"></span><span id="mp_removal_manual"></span>**MP\_REMOVAL\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="e0430-112">Manual.</span><span class="sxs-lookup"><span data-stu-id="e0430-112">Manual.</span></span>

</dd> <dt>

<span data-ttu-id="e0430-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**\_eliminación \_ automática de MP**</span><span class="sxs-lookup"><span data-stu-id="e0430-113"><span id="MP_REMOVAL_AUTOMATIC"></span><span id="mp_removal_automatic"></span>**MP\_REMOVAL\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="e0430-114">Automático.</span><span class="sxs-lookup"><span data-stu-id="e0430-114">Automatic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0430-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0430-115">Requirements</span></span>



| <span data-ttu-id="e0430-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0430-116">Requirement</span></span> | <span data-ttu-id="e0430-117">Value</span><span class="sxs-lookup"><span data-stu-id="e0430-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0430-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0430-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e0430-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0430-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e0430-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0430-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e0430-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0430-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0430-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0430-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0430-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0430-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





