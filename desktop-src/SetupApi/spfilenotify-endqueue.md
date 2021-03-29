---
description: La \_ notificación SPFILENOTIFY ENDQUEUE se envía a la rutina de devolución de llamada cuando se han completado todas las operaciones en cola.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: Mensaje de SPFILENOTIFY_ENDQUEUE (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3ed2ca896f91ec09cb49f89731b41c5d099465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002961"
---
# <a name="spfilenotify_endqueue-message"></a><span data-ttu-id="1f909-103">SPFILENOTIFY \_ ENDQUEUE</span><span class="sxs-lookup"><span data-stu-id="1f909-103">SPFILENOTIFY\_ENDQUEUE message</span></span>

<span data-ttu-id="1f909-104">La notificación **SPFILENOTIFY \_ ENDQUEUE** se envía a la rutina de devolución de llamada cuando se han completado todas las operaciones en cola.</span><span class="sxs-lookup"><span data-stu-id="1f909-104">The **SPFILENOTIFY\_ENDQUEUE** notification is sent to the callback routine when all of the queued operations have been completed.</span></span>


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="1f909-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f909-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f909-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="1f909-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="1f909-107">**True** si la cola se procesó correctamente; de lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="1f909-107">**TRUE** if the queue was processed successfully, **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="1f909-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="1f909-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="1f909-109">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="1f909-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f909-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f909-110">Return value</span></span>

<span data-ttu-id="1f909-111">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1f909-111">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f909-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f909-112">Requirements</span></span>



| <span data-ttu-id="1f909-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f909-113">Requirement</span></span> | <span data-ttu-id="1f909-114">Value</span><span class="sxs-lookup"><span data-stu-id="1f909-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f909-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f909-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1f909-116">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1f909-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1f909-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f909-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1f909-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f909-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f909-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f909-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f909-120"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f909-120"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f909-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f909-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f909-122">Información general</span><span class="sxs-lookup"><span data-stu-id="1f909-122">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="1f909-123">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="1f909-123">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="1f909-124">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="1f909-124">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="1f909-125">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="1f909-125">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




