---
description: La notificación de RENAMEERROR de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si se produce un error durante una operación de cambio de nombre de archivo.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: Mensaje de SPFILENOTIFY_RENAMEERROR (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361048"
---
# <a name="spfilenotify_renameerror-message"></a><span data-ttu-id="fdf88-103">SPFILENOTIFY \_ RENAMEERROR</span><span class="sxs-lookup"><span data-stu-id="fdf88-103">SPFILENOTIFY\_RENAMEERROR message</span></span>

<span data-ttu-id="fdf88-104">La notificación de **\_ RENAMEERROR de SPFILENOTIFY** se envía a la rutina de devolución de llamada si se produce un error durante una operación de cambio de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="fdf88-104">The **SPFILENOTIFY\_RENAMEERROR** notification is sent to the callback routine if an error occurs during a file rename operation.</span></span>


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="fdf88-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdf88-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdf88-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="fdf88-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="fdf88-107">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="fdf88-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="fdf88-108">El miembro **Win32Error** de la estructura **FILEPATHS** especifica el error que se produjo durante la operación de cambio de nombre.</span><span class="sxs-lookup"><span data-stu-id="fdf88-108">The **Win32Error** member of the **FILEPATHS** structure specifies the error that occurred during the rename operation.</span></span>

</dd> <dt>

<span data-ttu-id="fdf88-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="fdf88-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="fdf88-110">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="fdf88-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdf88-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdf88-111">Return value</span></span>

<span data-ttu-id="fdf88-112">La rutina de devolución de llamada debe devolver uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="fdf88-112">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="fdf88-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fdf88-113">Return code</span></span>                                                                                  | <span data-ttu-id="fdf88-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdf88-114">Description</span></span>                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fdf88-115"><dt>**FILEOP \_ reintentar**</dt></span><span class="sxs-lookup"><span data-stu-id="fdf88-115"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="fdf88-116">El usuario decidió volver a intentar la operación de cambio de nombre.</span><span class="sxs-lookup"><span data-stu-id="fdf88-116">The user chose to attempt the rename operation again.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="fdf88-117"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="fdf88-117"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="fdf88-118">El usuario decidió omitir la operación de cambio de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="fdf88-118">The user chose to skip the file rename operation.</span></span><br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="fdf88-119"><dt>**\_anulación de FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="fdf88-119"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="fdf88-120">Detenga la confirmación de la cola.</span><span class="sxs-lookup"><span data-stu-id="fdf88-120">Stop the queue commit.</span></span> <span data-ttu-id="fdf88-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="fdf88-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE**.</span></span> <span data-ttu-id="fdf88-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve información de error extendida, como error \_ cancelado (si el usuario canceló) o error \_ no \_ hay suficiente \_ memoria.</span><span class="sxs-lookup"><span data-stu-id="fdf88-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fdf88-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdf88-123">Requirements</span></span>



| <span data-ttu-id="fdf88-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdf88-124">Requirement</span></span> | <span data-ttu-id="fdf88-125">Value</span><span class="sxs-lookup"><span data-stu-id="fdf88-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf88-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdf88-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf88-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fdf88-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fdf88-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdf88-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf88-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fdf88-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fdf88-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdf88-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdf88-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf88-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdf88-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdf88-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdf88-133">Información general</span><span class="sxs-lookup"><span data-stu-id="fdf88-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="fdf88-134">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="fdf88-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="fdf88-135">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="fdf88-135">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="fdf88-136">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="fdf88-136">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="fdf88-137">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="fdf88-137">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

