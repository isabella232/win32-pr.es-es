---
description: La notificación de DELETEERROR de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si se produce un error durante una operación de eliminación de archivo.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: Mensaje de SPFILENOTIFY_DELETEERROR (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083390"
---
# <a name="spfilenotify_deleteerror-message"></a><span data-ttu-id="0cba1-103">SPFILENOTIFY \_ DELETEERROR</span><span class="sxs-lookup"><span data-stu-id="0cba1-103">SPFILENOTIFY\_DELETEERROR message</span></span>

<span data-ttu-id="0cba1-104">La notificación de **\_ DELETEERROR de SPFILENOTIFY** se envía a la rutina de devolución de llamada si se produce un error durante una operación de eliminación de archivo.</span><span class="sxs-lookup"><span data-stu-id="0cba1-104">The **SPFILENOTIFY\_DELETEERROR** notification is sent to the callback routine if an error occurs during a file delete operation.</span></span>


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="0cba1-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cba1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cba1-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="0cba1-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="0cba1-107">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="0cba1-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0cba1-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="0cba1-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="0cba1-109">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="0cba1-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cba1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cba1-110">Return value</span></span>

<span data-ttu-id="0cba1-111">La rutina de devolución de llamada debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0cba1-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="0cba1-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0cba1-112">Return code</span></span>                                                                                  | <span data-ttu-id="0cba1-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cba1-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0cba1-114"><dt>**\_anulación de FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="0cba1-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="0cba1-115">Se debe cancelar el procesamiento de la cola.</span><span class="sxs-lookup"><span data-stu-id="0cba1-115">Queue processing should be canceled.</span></span> <span data-ttu-id="0cba1-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve información de ERROR extendida como error \_ cancelado (si el usuario canceló) o error \_ no \_ hay suficiente \_ memoria.</span><span class="sxs-lookup"><span data-stu-id="0cba1-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="0cba1-117"><dt>**FILEOP \_ reintentar**</dt></span><span class="sxs-lookup"><span data-stu-id="0cba1-117"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="0cba1-118">El usuario está intentando de nuevo la operación de eliminación.</span><span class="sxs-lookup"><span data-stu-id="0cba1-118">The user is attempting the delete operation again.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="0cba1-119"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="0cba1-119"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="0cba1-120">El usuario está omitiendo la operación de eliminación de archivo.</span><span class="sxs-lookup"><span data-stu-id="0cba1-120">The user is skipping the file delete operation.</span></span><br/>                                                                                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="0cba1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cba1-121">Requirements</span></span>



| <span data-ttu-id="0cba1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cba1-122">Requirement</span></span> | <span data-ttu-id="0cba1-123">Value</span><span class="sxs-lookup"><span data-stu-id="0cba1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cba1-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cba1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0cba1-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0cba1-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0cba1-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cba1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0cba1-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0cba1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cba1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cba1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cba1-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cba1-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cba1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cba1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cba1-131">Información general</span><span class="sxs-lookup"><span data-stu-id="0cba1-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="0cba1-132">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="0cba1-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="0cba1-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="0cba1-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="0cba1-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="0cba1-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="0cba1-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="0cba1-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

