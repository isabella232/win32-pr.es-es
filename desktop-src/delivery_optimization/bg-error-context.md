---
title: Enumeración BG_ERROR_CONTEXT (Deliveryoptimization. h)
description: La enumeración BG_ERROR_CONTEXT define los valores constantes que especifican el contexto en el que se produjo el error.
ms.assetid: 86202343-5B5B-4A2E-A58D-7634BCB41E1C
keywords:
- Enumeración BG_ERROR_CONTEXT
topic_type:
- apiref
api_name:
- BG_ERROR_CONTEXT
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf6c68c20a5117e6cd8a02f8b4608b494c0ea93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490067"
---
# <a name="bg_error_context-enumeration"></a><span data-ttu-id="95e4b-104">Enumeración BG_ERROR_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="95e4b-104">BG_ERROR_CONTEXT enumeration</span></span>

<span data-ttu-id="95e4b-105">La enumeración **BG_ERROR_CONTEXT** define los valores constantes que especifican el contexto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="95e4b-105">The **BG_ERROR_CONTEXT** enumeration defines the constant values that specify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e4b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95e4b-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_ERROR_CONTEXT_NONE                        = 0,
  BG_ERROR_CONTEXT_UNKNOWN                     = 1,
  BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER       = 2,
  BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION  = 3,
  BG_ERROR_CONTEXT_LOCAL_FILE                  = 4,
  BG_ERROR_CONTEXT_REMOTE_FILE                 = 5,
  BG_ERROR_CONTEXT_GENERAL_TRANSPORT           = 6,
  BG_ERROR_CONTEXT_REMOTE_APPLICATION          = 7
} BG_ERROR_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="95e4b-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="95e4b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="95e4b-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span><span class="sxs-lookup"><span data-stu-id="95e4b-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="95e4b-109">No se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="95e4b-109">An error has not occurred.</span></span>

</dd> <dt>

<span data-ttu-id="95e4b-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="95e4b-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="95e4b-111">No se admite.</span><span class="sxs-lookup"><span data-stu-id="95e4b-111">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="95e4b-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span><span class="sxs-lookup"><span data-stu-id="95e4b-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="95e4b-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="95e4b-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="95e4b-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="95e4b-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="95e4b-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="95e4b-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="95e4b-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span><span class="sxs-lookup"><span data-stu-id="95e4b-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="95e4b-117">No se admite.</span><span class="sxs-lookup"><span data-stu-id="95e4b-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="95e4b-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span><span class="sxs-lookup"><span data-stu-id="95e4b-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="95e4b-119">El error estaba relacionado con el archivo remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="95e4b-119">The error was related to the specified remote file.</span></span> <span data-ttu-id="95e4b-120">Por ejemplo, la dirección URL no era accesible.</span><span class="sxs-lookup"><span data-stu-id="95e4b-120">For example, the URL was not accessible.</span></span>

</dd> <dt>

<span data-ttu-id="95e4b-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="95e4b-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span></span>
</dt> <dd>

<span data-ttu-id="95e4b-122">No se admite.</span><span class="sxs-lookup"><span data-stu-id="95e4b-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="95e4b-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span><span class="sxs-lookup"><span data-stu-id="95e4b-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="95e4b-124">No se admite.</span><span class="sxs-lookup"><span data-stu-id="95e4b-124">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95e4b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95e4b-125">Requirements</span></span>



| <span data-ttu-id="95e4b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="95e4b-126">Requirement</span></span> | <span data-ttu-id="95e4b-127">Value</span><span class="sxs-lookup"><span data-stu-id="95e4b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95e4b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95e4b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="95e4b-129">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="95e4b-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="95e4b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95e4b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="95e4b-131">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="95e4b-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="95e4b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95e4b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="95e4b-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="95e4b-133"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95e4b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="95e4b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e4b-135">**IBackgroundCopyError::GetError**</span><span class="sxs-lookup"><span data-stu-id="95e4b-135">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





