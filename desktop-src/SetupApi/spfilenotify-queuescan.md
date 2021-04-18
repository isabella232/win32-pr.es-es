---
description: La notificación de QUEUESCAN de SPFILENOTIFY \_ se envía a una rutina de devolución de llamada por SetupScanFileQueue para cada nodo de la subcola de copia de la cola de archivos. Esto solo se produce si se llamó a la función SetupScanFileQueue especificando la marca SPQ \_ scan \_ use \_ callback.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: Mensaje de SPFILENOTIFY_QUEUESCAN (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668174"
---
# <a name="spfilenotify_queuescan-message"></a><span data-ttu-id="9a746-104">SPFILENOTIFY \_ QUEUESCAN</span><span class="sxs-lookup"><span data-stu-id="9a746-104">SPFILENOTIFY\_QUEUESCAN message</span></span>

<span data-ttu-id="9a746-105">La notificación de **\_ QUEUESCAN de SPFILENOTIFY** se envía a una rutina de devolución de llamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nodo de la subcola de copia de la cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="9a746-105">The **SPFILENOTIFY\_QUEUESCAN** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="9a746-106">Esto solo se produce si se llamó a la función **SetupScanFileQueue** especificando la marca SPQ \_ scan \_ use \_ callback.</span><span class="sxs-lookup"><span data-stu-id="9a746-106">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a><span data-ttu-id="9a746-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a746-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a746-108">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="9a746-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="9a746-109">Cadena terminada en null que especifica la información de la ruta de acceso de destino para el archivo en cola en el nodo actual.</span><span class="sxs-lookup"><span data-stu-id="9a746-109">Null-terminated string that specifies the target path information for the file queued in the current node.</span></span>

</dd> <dt>

<span data-ttu-id="9a746-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="9a746-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="9a746-111">Si el archivo del nodo actual de la cola está en uso, *parám2* toma el valor SPQ \_ copia retrasada \_ .</span><span class="sxs-lookup"><span data-stu-id="9a746-111">If the file in the current node of the queue is in use, *Param2* takes the value SPQ\_DELAYED\_COPY.</span></span> <span data-ttu-id="9a746-112">Si el archivo no está en uso, el valor es cero.</span><span class="sxs-lookup"><span data-stu-id="9a746-112">If the file is not in use, the value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a746-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a746-113">Return value</span></span>

<span data-ttu-id="9a746-114">La rutina de devolución de llamada debe devolver un [código de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9a746-114">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="9a746-115">Si la rutina de devolución de llamada NO devuelve ningún \_ error, el análisis de cola continúa.</span><span class="sxs-lookup"><span data-stu-id="9a746-115">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="9a746-116">Si la rutina devuelve cualquier otro código de error, el análisis de cola se anula y [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="9a746-116">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="9a746-117">La función [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) no controla esta notificación.</span><span class="sxs-lookup"><span data-stu-id="9a746-117">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a746-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a746-118">Requirements</span></span>



| <span data-ttu-id="9a746-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a746-119">Requirement</span></span> | <span data-ttu-id="9a746-120">Value</span><span class="sxs-lookup"><span data-stu-id="9a746-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a746-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a746-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9a746-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9a746-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9a746-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a746-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9a746-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a746-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a746-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a746-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a746-126"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a746-126"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a746-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a746-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a746-128">Información general</span><span class="sxs-lookup"><span data-stu-id="9a746-128">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="9a746-129">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="9a746-129">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="9a746-130">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="9a746-130">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

