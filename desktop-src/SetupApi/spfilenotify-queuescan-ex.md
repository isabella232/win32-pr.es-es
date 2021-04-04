---
description: La \_ notificación SPFILENOTIFY QUEUESCAN \_ ex se envía a una rutina de devolución de llamada por SetupScanFileQueue para cada nodo de la subcola de copia de la cola de archivos.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Mensaje de SPFILENOTIFY_QUEUESCAN_EX (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908809"
---
# <a name="spfilenotify_queuescan_ex-message"></a><span data-ttu-id="d7bf0-103">SPFILENOTIFY \_ QUEUESCAN \_ ex</span><span class="sxs-lookup"><span data-stu-id="d7bf0-103">SPFILENOTIFY\_QUEUESCAN\_EX message</span></span>

<span data-ttu-id="d7bf0-104">La notificación **SPFILENOTIFY \_ QUEUESCAN \_ ex** se envía a una rutina de devolución de llamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nodo de la subcola de copia de la cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="d7bf0-104">The **SPFILENOTIFY\_QUEUESCAN\_EX** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="d7bf0-105">Esto solo se produce si se llamó a la función **SetupScanFileQueue** especificando la marca SPQ \_ scan \_ use \_ CALLBACKEX.</span><span class="sxs-lookup"><span data-stu-id="d7bf0-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACKEX.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="d7bf0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7bf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7bf0-107">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="d7bf0-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="d7bf0-108">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="d7bf0-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="d7bf0-109">El miembro de **destino** es el nombre de archivo del archivo de destino en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d7bf0-109">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="d7bf0-110">El miembro de **origen** es la ruta de acceso esperada del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="d7bf0-110">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="d7bf0-111">El miembro **Win32Error** es el error de firma.</span><span class="sxs-lookup"><span data-stu-id="d7bf0-111">The **Win32Error** member is the signing error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7bf0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7bf0-112">Return value</span></span>

<span data-ttu-id="d7bf0-113">La rutina de devolución de llamada debe devolver un [código de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d7bf0-113">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="d7bf0-114">Si la rutina de devolución de llamada NO devuelve ningún \_ error, el análisis de cola continúa.</span><span class="sxs-lookup"><span data-stu-id="d7bf0-114">If the callback routine returns NO\_ERROR, the queue scan continues.</span></span> <span data-ttu-id="d7bf0-115">Si la rutina devuelve cualquier otro código de error, el análisis de cola se anula y [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) devuelve false.</span><span class="sxs-lookup"><span data-stu-id="d7bf0-115">If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="d7bf0-116">La función [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) no controla esta notificación.</span><span class="sxs-lookup"><span data-stu-id="d7bf0-116">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7bf0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7bf0-117">Requirements</span></span>



| <span data-ttu-id="d7bf0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7bf0-118">Requirement</span></span> | <span data-ttu-id="d7bf0-119">Value</span><span class="sxs-lookup"><span data-stu-id="d7bf0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bf0-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7bf0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d7bf0-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d7bf0-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d7bf0-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7bf0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d7bf0-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7bf0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7bf0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7bf0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7bf0-125"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7bf0-125"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7bf0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7bf0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bf0-127">Información general</span><span class="sxs-lookup"><span data-stu-id="d7bf0-127">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="d7bf0-128">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="d7bf0-128">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="d7bf0-129">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="d7bf0-129">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

