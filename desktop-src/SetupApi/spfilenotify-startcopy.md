---
description: La notificación de STARTCOPY de SPFILENOTIFY \_ se envía a la función de devolución de llamada cuando la cola inicia una operación de copia de archivos.
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: Mensaje de SPFILENOTIFY_STARTCOPY (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6693938a2f67530e7e3c906c5105d2c98a915a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668173"
---
# <a name="spfilenotify_startcopy-message"></a><span data-ttu-id="4d7aa-103">SPFILENOTIFY \_ STARTCOPY</span><span class="sxs-lookup"><span data-stu-id="4d7aa-103">SPFILENOTIFY\_STARTCOPY message</span></span>

<span data-ttu-id="4d7aa-104">La notificación de **\_ STARTCOPY de SPFILENOTIFY** se envía a la función de devolución de llamada cuando la cola inicia una operación de copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="4d7aa-104">The **SPFILENOTIFY\_STARTCOPY** notification is sent to the callback function when the queue starts a file copy operation.</span></span>


```C++
SPFILENOTIFY_STARTCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="4d7aa-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d7aa-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7aa-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="4d7aa-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="4d7aa-107">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="4d7aa-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4d7aa-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="4d7aa-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="4d7aa-109">Siempre tiene el valor FILEOP \_ copiar.</span><span class="sxs-lookup"><span data-stu-id="4d7aa-109">Always has the value FILEOP\_COPY.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d7aa-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d7aa-110">Return value</span></span>

<span data-ttu-id="4d7aa-111">La rutina de devolución de llamada debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4d7aa-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="4d7aa-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4d7aa-112">Return code</span></span>                                                                                  | <span data-ttu-id="4d7aa-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d7aa-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d7aa-114"><dt>**\_anulación de FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="4d7aa-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="4d7aa-115">Anular el proceso de confirmación de la cola.</span><span class="sxs-lookup"><span data-stu-id="4d7aa-115">Abort the queue commit process.</span></span> <span data-ttu-id="4d7aa-116">La rutina de devolución de llamada debe llamar a [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para indicar el motivo de la terminación.</span><span class="sxs-lookup"><span data-stu-id="4d7aa-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for termination.</span></span> <span data-ttu-id="4d7aa-117">La función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve **false** y una llamada subsiguiente a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error establecido por la rutina de devolución de llamada durante la llamada a **SetLastError**.</span><span class="sxs-lookup"><span data-stu-id="4d7aa-117">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="4d7aa-118"><dt>**FILEOP \_ Doit**</dt></span><span class="sxs-lookup"><span data-stu-id="4d7aa-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="4d7aa-119">Realice la operación de copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="4d7aa-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="4d7aa-120"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="4d7aa-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="4d7aa-121">Omitir la operación de copia actual.</span><span class="sxs-lookup"><span data-stu-id="4d7aa-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="4d7aa-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d7aa-122">Requirements</span></span>



| <span data-ttu-id="4d7aa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d7aa-123">Requirement</span></span> | <span data-ttu-id="4d7aa-124">Value</span><span class="sxs-lookup"><span data-stu-id="4d7aa-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7aa-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d7aa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4d7aa-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4d7aa-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4d7aa-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d7aa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4d7aa-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d7aa-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d7aa-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d7aa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d7aa-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d7aa-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7aa-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d7aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7aa-132">Información general</span><span class="sxs-lookup"><span data-stu-id="4d7aa-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="4d7aa-133">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="4d7aa-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="4d7aa-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="4d7aa-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="4d7aa-135">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="4d7aa-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="4d7aa-136">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="4d7aa-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

