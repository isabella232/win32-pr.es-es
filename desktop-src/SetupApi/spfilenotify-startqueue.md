---
description: La notificación de STARTQUEUE de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada cuando se inicia el proceso de compromiso de cola.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: Mensaje de SPFILENOTIFY_STARTQUEUE (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090e3f97dceb1843d75934dd99cca500e6f93086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668172"
---
# <a name="spfilenotify_startqueue-message"></a><span data-ttu-id="09a53-103">SPFILENOTIFY \_ STARTQUEUE</span><span class="sxs-lookup"><span data-stu-id="09a53-103">SPFILENOTIFY\_STARTQUEUE message</span></span>

<span data-ttu-id="09a53-104">La notificación de **\_ STARTQUEUE de SPFILENOTIFY** se envía a la rutina de devolución de llamada cuando se inicia el proceso de compromiso de cola.</span><span class="sxs-lookup"><span data-stu-id="09a53-104">The **SPFILENOTIFY\_STARTQUEUE** notification is sent to the callback routine when the queue commitment process starts.</span></span>


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="09a53-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09a53-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09a53-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="09a53-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="09a53-107">Identificador de la ventana que va a ser propietaria de los cuadros de diálogo generados por la rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="09a53-107">Handle to the window that is to own the dialog boxes that the callback routine generates.</span></span>

</dd> <dt>

<span data-ttu-id="09a53-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="09a53-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="09a53-109">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="09a53-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09a53-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09a53-110">Return value</span></span>

<span data-ttu-id="09a53-111">Si se produce un error, la rutina de devolución de llamada debe llamar a [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), especificar el error y, a continuación, devolver cero.</span><span class="sxs-lookup"><span data-stu-id="09a53-111">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="09a53-112">La función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devolverá **false** y una llamada subsiguiente a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el código de error establecido por la rutina de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="09a53-112">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="09a53-113">Si no se produce ningún error, la rutina de devolución de llamada debe devolver un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="09a53-113">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a53-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09a53-114">Requirements</span></span>



| <span data-ttu-id="09a53-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="09a53-115">Requirement</span></span> | <span data-ttu-id="09a53-116">Value</span><span class="sxs-lookup"><span data-stu-id="09a53-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09a53-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09a53-117">Minimum supported client</span></span><br/> | <span data-ttu-id="09a53-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="09a53-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="09a53-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09a53-119">Minimum supported server</span></span><br/> | <span data-ttu-id="09a53-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="09a53-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09a53-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09a53-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="09a53-122"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="09a53-122"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09a53-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="09a53-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a53-124">Información general</span><span class="sxs-lookup"><span data-stu-id="09a53-124">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="09a53-125">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="09a53-125">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="09a53-126">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="09a53-126">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="09a53-127">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="09a53-127">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

