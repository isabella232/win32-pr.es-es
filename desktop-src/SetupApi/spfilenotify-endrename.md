---
description: La \_ notificación SPFILENOTIFY ENDRENAME se envía a la rutina de devolución de llamada cuando la cola completa una operación de cambio de nombre. Esta notificación se envía incluso si el usuario cancela o si se produce un error.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: Mensaje de SPFILENOTIFY_ENDRENAME (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a316d4dfe72ee9eb7d85fdb70eb90e1cf3d3f463
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669785"
---
# <a name="spfilenotify_endrename-message"></a><span data-ttu-id="803b1-104">SPFILENOTIFY \_ ENDRENAME</span><span class="sxs-lookup"><span data-stu-id="803b1-104">SPFILENOTIFY\_ENDRENAME message</span></span>

<span data-ttu-id="803b1-105">La notificación **SPFILENOTIFY \_ ENDRENAME** se envía a la rutina de devolución de llamada cuando la cola completa una operación de cambio de nombre.</span><span class="sxs-lookup"><span data-stu-id="803b1-105">The **SPFILENOTIFY\_ENDRENAME** notification is sent to the callback routine when the queue completes a rename operation.</span></span> <span data-ttu-id="803b1-106">Esta notificación se envía incluso si el usuario cancela o si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="803b1-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="803b1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="803b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="803b1-108">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="803b1-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="803b1-109">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="803b1-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="803b1-110">El miembro **Win32Error** de la estructura **FILEPATHS** indica el resultado de la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="803b1-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="803b1-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="803b1-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="803b1-112">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="803b1-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="803b1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="803b1-113">Return value</span></span>

<span data-ttu-id="803b1-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="803b1-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="803b1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="803b1-115">Requirements</span></span>



| <span data-ttu-id="803b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="803b1-116">Requirement</span></span> | <span data-ttu-id="803b1-117">Value</span><span class="sxs-lookup"><span data-stu-id="803b1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="803b1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="803b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="803b1-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="803b1-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="803b1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="803b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="803b1-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="803b1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="803b1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="803b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="803b1-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="803b1-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803b1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="803b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803b1-125">Información general</span><span class="sxs-lookup"><span data-stu-id="803b1-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="803b1-126">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="803b1-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="803b1-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="803b1-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="803b1-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="803b1-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="803b1-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="803b1-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




