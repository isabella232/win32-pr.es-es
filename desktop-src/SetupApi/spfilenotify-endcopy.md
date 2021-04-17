---
description: La \_ notificación SPFILENOTIFY ENDCOPY se pasa a la función de devolución de llamada cuando la cola completa una operación de copia. Esta notificación se envía incluso si el usuario cancela o si se produce un error.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: Mensaje de SPFILENOTIFY_ENDCOPY (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75dba56c4a38ac87003a3b59b594135e55a462f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669985"
---
# <a name="spfilenotify_endcopy-message"></a><span data-ttu-id="540db-104">SPFILENOTIFY \_ ENDCOPY</span><span class="sxs-lookup"><span data-stu-id="540db-104">SPFILENOTIFY\_ENDCOPY message</span></span>

<span data-ttu-id="540db-105">La notificación **SPFILENOTIFY \_ ENDCOPY** se pasa a la función de devolución de llamada cuando la cola completa una operación de copia.</span><span class="sxs-lookup"><span data-stu-id="540db-105">The **SPFILENOTIFY\_ENDCOPY** notification is passed to the callback function when the queue completes a copy operation.</span></span> <span data-ttu-id="540db-106">Esta notificación se envía incluso si el usuario cancela o si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="540db-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="540db-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="540db-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="540db-108">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="540db-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="540db-109">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="540db-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="540db-110">El miembro **Win32Error** de la estructura **FILEPATHS** indica el resultado de la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="540db-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="540db-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="540db-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="540db-112">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="540db-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="540db-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="540db-113">Return value</span></span>

<span data-ttu-id="540db-114">Se omite el código de retorno.</span><span class="sxs-lookup"><span data-stu-id="540db-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="540db-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="540db-115">Requirements</span></span>



| <span data-ttu-id="540db-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="540db-116">Requirement</span></span> | <span data-ttu-id="540db-117">Value</span><span class="sxs-lookup"><span data-stu-id="540db-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="540db-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="540db-118">Minimum supported client</span></span><br/> | <span data-ttu-id="540db-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="540db-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="540db-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="540db-120">Minimum supported server</span></span><br/> | <span data-ttu-id="540db-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="540db-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="540db-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="540db-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="540db-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="540db-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="540db-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="540db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="540db-125">Información general</span><span class="sxs-lookup"><span data-stu-id="540db-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="540db-126">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="540db-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="540db-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="540db-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="540db-128">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="540db-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="540db-129">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="540db-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




