---
description: La notificación de ENDSUBQUEUE de SPFILENOTIFY \_ se envía a la función de devolución de llamada cuando la cola completa todas las operaciones de la subcola de eliminación, cambio de nombre o copia.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: Mensaje de SPFILENOTIFY_ENDSUBQUEUE (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083388"
---
# <a name="spfilenotify_endsubqueue-message"></a><span data-ttu-id="da8be-103">SPFILENOTIFY \_ ENDSUBQUEUE</span><span class="sxs-lookup"><span data-stu-id="da8be-103">SPFILENOTIFY\_ENDSUBQUEUE message</span></span>

<span data-ttu-id="da8be-104">La notificación de **\_ ENDSUBQUEUE de SPFILENOTIFY** se envía a la función de devolución de llamada cuando la cola completa todas las operaciones de la subcola de eliminación, cambio de nombre o copia.</span><span class="sxs-lookup"><span data-stu-id="da8be-104">The **SPFILENOTIFY\_ENDSUBQUEUE** notification is sent to the callback function when the queue completes all the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="da8be-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da8be-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da8be-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="da8be-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="da8be-107">Subcola que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="da8be-107">Subqueue that has been completed.</span></span> <span data-ttu-id="da8be-108">Este parámetro puede ser uno de los siguientes valores FILEOP \_ Delete, FILEOP \_ Rename o FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="da8be-108">This parameter can be one of the following values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="da8be-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="da8be-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="da8be-110">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="da8be-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da8be-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da8be-111">Return value</span></span>

<span data-ttu-id="da8be-112">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="da8be-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="da8be-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da8be-113">Requirements</span></span>



| <span data-ttu-id="da8be-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="da8be-114">Requirement</span></span> | <span data-ttu-id="da8be-115">Value</span><span class="sxs-lookup"><span data-stu-id="da8be-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da8be-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da8be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da8be-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="da8be-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="da8be-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da8be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da8be-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="da8be-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da8be-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da8be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="da8be-121"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="da8be-121"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da8be-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="da8be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8be-123">Información general</span><span class="sxs-lookup"><span data-stu-id="da8be-123">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="da8be-124">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="da8be-124">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="da8be-125">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="da8be-125">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="da8be-126">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="da8be-126">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




