---
description: La notificación de STARTSUBQUEUE de SPFILENOTIFY \_ se envía a la función de devolución de llamada cuando la cola comienza a procesar las operaciones en la subcola de eliminación, cambio de nombre o copia.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Mensaje de SPFILENOTIFY_STARTSUBQUEUE (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669715"
---
# <a name="spfilenotify_startsubqueue-message"></a><span data-ttu-id="d5175-103">SPFILENOTIFY \_ STARTSUBQUEUE</span><span class="sxs-lookup"><span data-stu-id="d5175-103">SPFILENOTIFY\_STARTSUBQUEUE message</span></span>

<span data-ttu-id="d5175-104">La notificación de **\_ STARTSUBQUEUE de SPFILENOTIFY** se envía a la función de devolución de llamada cuando la cola comienza a procesar las operaciones en la subcola de eliminación, cambio de nombre o copia.</span><span class="sxs-lookup"><span data-stu-id="d5175-104">The **SPFILENOTIFY\_STARTSUBQUEUE** notification is sent to the callback function when the queue starts to process the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a><span data-ttu-id="d5175-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5175-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5175-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="d5175-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="d5175-107">Subqueue que se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="d5175-107">Subqueue that has been started.</span></span> <span data-ttu-id="d5175-108">Este parámetro puede ser cualquiera de los valores FILEOP \_ Delete, FILEOP \_ Rename o FILEOP \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="d5175-108">This parameter can be any one of the values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="d5175-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="d5175-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="d5175-110">Número de operaciones de copia, cambio de nombre o eliminación de archivos en la subcola.</span><span class="sxs-lookup"><span data-stu-id="d5175-110">Number of file copy, rename, or delete operations in the subqueue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5175-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5175-111">Return value</span></span>

<span data-ttu-id="d5175-112">Si se produce un error, la rutina de devolución de llamada debe llamar a [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), especificar el error y, a continuación, devolver cero.</span><span class="sxs-lookup"><span data-stu-id="d5175-112">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="d5175-113">La función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devolverá **false** y una llamada subsiguiente a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el código de error establecido por la rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d5175-113">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="d5175-114">Si no se produce ningún error, la rutina de devolución de llamada debe devolver un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d5175-114">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5175-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5175-115">Requirements</span></span>



| <span data-ttu-id="d5175-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5175-116">Requirement</span></span> | <span data-ttu-id="d5175-117">Value</span><span class="sxs-lookup"><span data-stu-id="d5175-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5175-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5175-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d5175-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d5175-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d5175-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5175-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d5175-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5175-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5175-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5175-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5175-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5175-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5175-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5175-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5175-125">Información general</span><span class="sxs-lookup"><span data-stu-id="d5175-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="d5175-126">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="d5175-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="d5175-127">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="d5175-127">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="d5175-128">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="d5175-128">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

