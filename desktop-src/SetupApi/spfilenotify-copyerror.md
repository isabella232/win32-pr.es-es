---
description: La notificación de COPYERROR de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si se produce un error durante una operación de copia de archivos.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: Mensaje de SPFILENOTIFY_COPYERROR (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910333"
---
# <a name="spfilenotify_copyerror-message"></a><span data-ttu-id="30250-103">SPFILENOTIFY \_ COPYERROR</span><span class="sxs-lookup"><span data-stu-id="30250-103">SPFILENOTIFY\_COPYERROR message</span></span>

<span data-ttu-id="30250-104">La notificación de **\_ COPYERROR de SPFILENOTIFY** se envía a la rutina de devolución de llamada si se produce un error durante una operación de copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="30250-104">The **SPFILENOTIFY\_COPYERROR** notification is sent to the callback routine if an error occurs during a file copy operation.</span></span>


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a><span data-ttu-id="30250-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30250-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30250-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="30250-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="30250-107">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="30250-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="30250-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="30250-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="30250-109">Puntero a un búfer, de tamaño máximo de \_ caracteres de ruta de acceso, que almacena la nueva información de ruta de acceso especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="30250-109">Pointer to a buffer, of size MAX\_PATH characters, that stores new path information specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30250-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30250-110">Return value</span></span>

<span data-ttu-id="30250-111">La devolución de llamada debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="30250-111">The callback should return one of the following values.</span></span>



| <span data-ttu-id="30250-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="30250-112">Return code</span></span>                                                                                    | <span data-ttu-id="30250-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="30250-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="30250-114"><dt>**\_anulación de FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="30250-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="30250-115">Se debe cancelar el procesamiento de la cola.</span><span class="sxs-lookup"><span data-stu-id="30250-115">Queue processing should be canceled.</span></span> <span data-ttu-id="30250-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve cero y [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve información de ERROR extendida como error \_ cancelado (si el usuario canceló) o error \_ no \_ hay suficiente \_ memoria.</span><span class="sxs-lookup"><span data-stu-id="30250-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="30250-117"><dt>**FILEOP \_ NEWPATH**</dt></span><span class="sxs-lookup"><span data-stu-id="30250-117"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="30250-118">Vuelva a intentar la operación de copia mediante la ruta de acceso de la función de devolución de llamada colocada en el búfer al que apunta el parámetro *parám2* .</span><span class="sxs-lookup"><span data-stu-id="30250-118">Retry the copy operation using the path the callback function placed in the buffer pointed to by the *Param2* parameter.</span></span> <span data-ttu-id="30250-119">La rutina de devolución de llamada debe asegurarse de que la ruta de acceso no desborda el tamaño de búfer de una matriz TCHAR de \_ elementos de ruta de acceso máxima.</span><span class="sxs-lookup"><span data-stu-id="30250-119">The callback routine should ensure that the path does not overflow the buffer size of a TCHAR array of MAX\_PATH elements.</span></span><br/>                |
| <dl> <span data-ttu-id="30250-120"><dt>**FILEOP \_ reintentar**</dt></span><span class="sxs-lookup"><span data-stu-id="30250-120"><dt>**FILEOP\_RETRY**</dt></span></span> </dl>   | <span data-ttu-id="30250-121">El usuario está intentando volver a realizar la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="30250-121">The user is attempting the copy operation again.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="30250-122"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="30250-122"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="30250-123">El usuario está omitiendo la operación de copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="30250-123">The user is skipping the file copy operation.</span></span><br/>                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="30250-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30250-124">Requirements</span></span>



| <span data-ttu-id="30250-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="30250-125">Requirement</span></span> | <span data-ttu-id="30250-126">Value</span><span class="sxs-lookup"><span data-stu-id="30250-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30250-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30250-127">Minimum supported client</span></span><br/> | <span data-ttu-id="30250-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="30250-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="30250-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30250-129">Minimum supported server</span></span><br/> | <span data-ttu-id="30250-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="30250-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30250-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30250-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="30250-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="30250-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30250-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="30250-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30250-134">Información general</span><span class="sxs-lookup"><span data-stu-id="30250-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="30250-135">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="30250-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="30250-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="30250-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="30250-137">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="30250-137">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="30250-138">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="30250-138">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

