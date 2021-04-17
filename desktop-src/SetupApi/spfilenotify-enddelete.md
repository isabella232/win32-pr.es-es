---
description: La \_ notificación SPFILENOTIFY ENDDELETE se devuelve a la rutina de devolución de llamada cuando una cola completa una operación de eliminación. Esta notificación se envía incluso si el usuario cancela o si se produce un error.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: Mensaje de SPFILENOTIFY_ENDDELETE (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ee4762dc33f8b8ec16a6be273cb42f41aeafce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669788"
---
# <a name="spfilenotify_enddelete-message"></a><span data-ttu-id="84c43-104">SPFILENOTIFY \_ ENDDELETE</span><span class="sxs-lookup"><span data-stu-id="84c43-104">SPFILENOTIFY\_ENDDELETE message</span></span>

<span data-ttu-id="84c43-105">La notificación **SPFILENOTIFY \_ ENDDELETE** se devuelve a la rutina de devolución de llamada cuando una cola completa una operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="84c43-105">The **SPFILENOTIFY\_ENDDELETE** notification is returned to the callback routine when a queue completes a delete operation.</span></span> <span data-ttu-id="84c43-106">Esta notificación se envía incluso si el usuario cancela o si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="84c43-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="84c43-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84c43-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c43-108">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="84c43-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="84c43-109">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="84c43-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="84c43-110">El miembro **Win32Error** de la estructura **FILEPATHS** indica el resultado de una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="84c43-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of a copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="84c43-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="84c43-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="84c43-112">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="84c43-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c43-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84c43-113">Return value</span></span>

<span data-ttu-id="84c43-114">Se omite el código de retorno.</span><span class="sxs-lookup"><span data-stu-id="84c43-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c43-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84c43-115">Requirements</span></span>



| <span data-ttu-id="84c43-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="84c43-116">Requirement</span></span> | <span data-ttu-id="84c43-117">Value</span><span class="sxs-lookup"><span data-stu-id="84c43-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84c43-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84c43-118">Minimum supported client</span></span><br/> | <span data-ttu-id="84c43-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="84c43-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="84c43-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84c43-120">Minimum supported server</span></span><br/> | <span data-ttu-id="84c43-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="84c43-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84c43-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84c43-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="84c43-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="84c43-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84c43-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="84c43-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c43-125">Información general</span><span class="sxs-lookup"><span data-stu-id="84c43-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="84c43-126">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="84c43-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="84c43-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="84c43-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="84c43-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="84c43-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="84c43-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="84c43-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




