---
title: MPCLEAN_PRECHECK_DATA estructura (MpClient. h)
description: Datos de notificación pasados a la función de devolución de llamada de precomprobación limpia.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCLEAN_PRECHECK_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490007"
---
# <a name="mpclean_precheck_data-structure"></a><span data-ttu-id="4353a-105">Estructura de datos de \_ comprobación de MPCLEAN \_</span><span class="sxs-lookup"><span data-stu-id="4353a-105">MPCLEAN\_PRECHECK\_DATA structure</span></span>

<span data-ttu-id="4353a-106">Datos de notificación pasados a la función de devolución de llamada de precomprobación limpia.</span><span class="sxs-lookup"><span data-stu-id="4353a-106">Notification data passed to clean precheck callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4353a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4353a-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a><span data-ttu-id="4353a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4353a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4353a-109">**BlockedResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="4353a-109">**BlockedResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="4353a-110">Tipo: **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="4353a-110">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="4353a-111">Información de recursos sobre el recurso que se está bloqueando.</span><span class="sxs-lookup"><span data-stu-id="4353a-111">Resource information about the resource being blocked.</span></span> <span data-ttu-id="4353a-112">Por ejemplo, cuando el progreso es **MPNOTIFY \_ precomprobar \_ recurso \_ bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="4353a-112">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="4353a-113">Vea [**\_ información de MPRESOURCE**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="4353a-113">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="4353a-114">**información de PMPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="4353a-114">**PMPRESOURCE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="4353a-115">Tipo: **BlockingResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="4353a-115">Type: **BlockingResourceInfo**</span></span>

</dd> <dd>

<span data-ttu-id="4353a-116">Información de recursos sobre el recurso que está bloqueando.</span><span class="sxs-lookup"><span data-stu-id="4353a-116">Resource information about the resource that is blocking.</span></span> <span data-ttu-id="4353a-117">Por ejemplo, cuando el progreso es **MPNOTIFY \_ precomprobar \_ recurso \_ bloqueado**.</span><span class="sxs-lookup"><span data-stu-id="4353a-117">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="4353a-118">Vea [**\_ información de MPRESOURCE**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="4353a-118">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4353a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4353a-119">Requirements</span></span>



| <span data-ttu-id="4353a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4353a-120">Requirement</span></span> | <span data-ttu-id="4353a-121">Value</span><span class="sxs-lookup"><span data-stu-id="4353a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4353a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4353a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4353a-123">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4353a-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4353a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4353a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4353a-125">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4353a-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4353a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4353a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4353a-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4353a-127"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4353a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4353a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4353a-129">**información de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="4353a-129">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





