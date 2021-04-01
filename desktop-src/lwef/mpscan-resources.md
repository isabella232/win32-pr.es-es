---
title: MPSCAN_RESOURCES estructura (MpClient. h)
description: Información de recursos pasada durante una operación de examen.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSCAN_RESOURCES características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997119"
---
# <a name="mpscan_resources-structure"></a><span data-ttu-id="ae784-105">\_Estructura de recursos MPSCAN</span><span class="sxs-lookup"><span data-stu-id="ae784-105">MPSCAN\_RESOURCES structure</span></span>

<span data-ttu-id="ae784-106">Información de recursos pasada durante una operación de examen.</span><span class="sxs-lookup"><span data-stu-id="ae784-106">Resource information passed during a scan operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae784-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae784-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a><span data-ttu-id="ae784-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae784-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ae784-109">**dwResourceCount**</span><span class="sxs-lookup"><span data-stu-id="ae784-109">**dwResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="ae784-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="ae784-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="ae784-111">Recuento de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae784-111">Count of resources.</span></span>

</dd> <dt>

<span data-ttu-id="ae784-112">**pResourceList**</span><span class="sxs-lookup"><span data-stu-id="ae784-112">**pResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="ae784-113">Tipo: **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="ae784-113">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="ae784-114">Matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae784-114">Array of resources.</span></span> <span data-ttu-id="ae784-115">Vea [**\_ información de MPRESOURCE**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="ae784-115">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae784-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae784-116">Requirements</span></span>



| <span data-ttu-id="ae784-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae784-117">Requirement</span></span> | <span data-ttu-id="ae784-118">Value</span><span class="sxs-lookup"><span data-stu-id="ae784-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae784-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae784-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae784-120">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae784-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ae784-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae784-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae784-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae784-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae784-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae784-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae784-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae784-124"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae784-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae784-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae784-126">**información de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="ae784-126">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





