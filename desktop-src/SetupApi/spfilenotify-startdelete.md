---
description: La notificación de STARTDELETE de SPFILENOTIFY \_ se envía a la función de devolución de llamada cuando la cola inicia una operación de eliminación de archivo.
ms.assetid: 244714ad-dde7-4b5a-b3f3-78aa4cc901f5
title: Mensaje de SPFILENOTIFY_STARTDELETE (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a4a0d362a1c1c3824154fb02e0bb9cf01b24d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546387"
---
# <a name="spfilenotify_startdelete-message"></a><span data-ttu-id="13f7e-103">SPFILENOTIFY \_ STARTDELETE</span><span class="sxs-lookup"><span data-stu-id="13f7e-103">SPFILENOTIFY\_STARTDELETE message</span></span>

<span data-ttu-id="13f7e-104">La notificación de **\_ STARTDELETE de SPFILENOTIFY** se envía a la función de devolución de llamada cuando la cola inicia una operación de eliminación de archivo.</span><span class="sxs-lookup"><span data-stu-id="13f7e-104">The **SPFILENOTIFY\_STARTDELETE** notification is sent to the callback function when the queue starts a file delete operation.</span></span>


```C++
SPFILENOTIFY_STARTDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="13f7e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13f7e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f7e-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="13f7e-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="13f7e-107">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="13f7e-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="13f7e-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="13f7e-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="13f7e-109">Siempre tiene el valor FILEOP \_ eliminar.</span><span class="sxs-lookup"><span data-stu-id="13f7e-109">Always has the value FILEOP\_DELETE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f7e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13f7e-110">Return value</span></span>

<span data-ttu-id="13f7e-111">La rutina de devolución de llamada debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="13f7e-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="13f7e-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="13f7e-112">Return code</span></span>                                                                                  | <span data-ttu-id="13f7e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="13f7e-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13f7e-114"><dt>**\_anulación de FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="13f7e-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="13f7e-115">Anule la confirmación de la cola.</span><span class="sxs-lookup"><span data-stu-id="13f7e-115">Abort the queue commit.</span></span> <span data-ttu-id="13f7e-116">La rutina de devolución de llamada debe llamar a [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) para indicar el motivo de la anulación.</span><span class="sxs-lookup"><span data-stu-id="13f7e-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for aborting.</span></span> <span data-ttu-id="13f7e-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve **false** y una llamada subsiguiente a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el código de error establecido por la rutina de devolución de llamada durante la llamada a **SetLastError**.</span><span class="sxs-lookup"><span data-stu-id="13f7e-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="13f7e-118"><dt>**FILEOP \_ Doit**</dt></span><span class="sxs-lookup"><span data-stu-id="13f7e-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="13f7e-119">Realice la operación de copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="13f7e-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="13f7e-120"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="13f7e-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="13f7e-121">Omitir la operación de copia actual.</span><span class="sxs-lookup"><span data-stu-id="13f7e-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="13f7e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13f7e-122">Requirements</span></span>



| <span data-ttu-id="13f7e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="13f7e-123">Requirement</span></span> | <span data-ttu-id="13f7e-124">Value</span><span class="sxs-lookup"><span data-stu-id="13f7e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13f7e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13f7e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="13f7e-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="13f7e-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="13f7e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13f7e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="13f7e-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="13f7e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="13f7e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13f7e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="13f7e-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="13f7e-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f7e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="13f7e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f7e-132">Información general</span><span class="sxs-lookup"><span data-stu-id="13f7e-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="13f7e-133">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="13f7e-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="13f7e-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="13f7e-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="13f7e-135">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="13f7e-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="13f7e-136">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="13f7e-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

