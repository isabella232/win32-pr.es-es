---
description: La notificación de NEEDMEDIA de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada cuando se requieren nuevos medios o un nuevo archivo. cab.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: Mensaje de SPFILENOTIFY_NEEDMEDIA (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670073"
---
# <a name="spfilenotify_needmedia-message"></a><span data-ttu-id="f8f4b-103">SPFILENOTIFY \_ NEEDMEDIA</span><span class="sxs-lookup"><span data-stu-id="f8f4b-103">SPFILENOTIFY\_NEEDMEDIA message</span></span>

<span data-ttu-id="f8f4b-104">La notificación de **\_ NEEDMEDIA de SPFILENOTIFY** se envía a la rutina de devolución de llamada cuando se requieren nuevos medios o un nuevo archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-104">The **SPFILENOTIFY\_NEEDMEDIA** notification is sent to the callback routine when new media or a new cabinet file is required.</span></span>


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="f8f4b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8f4b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f4b-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="f8f4b-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="f8f4b-107">Puntero a una estructura de [**\_ medios de origen**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) .</span><span class="sxs-lookup"><span data-stu-id="f8f4b-107">Pointer to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f8f4b-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="f8f4b-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="f8f4b-109">Puntero a una matriz de caracteres para almacenar la nueva información de la ruta de acceso proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-109">Pointer to a character array to store new path information supplied by the user.</span></span> <span data-ttu-id="f8f4b-110">El tamaño del búfer es una matriz **TCHAR** de \_ elementos de ruta de acceso Max.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-110">The buffer size is a **TCHAR** array of MAX\_PATH elements.</span></span> <span data-ttu-id="f8f4b-111">La información de ruta de acceso devuelta por la aplicación de instalación no debe superar este tamaño.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-111">The path information returned by your setup application should not exceed this size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f4b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8f4b-112">Return value</span></span>

<span data-ttu-id="f8f4b-113">La rutina de devolución de llamada debe devolver uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-113">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="f8f4b-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f8f4b-114">Return code</span></span>                                                                                    | <span data-ttu-id="f8f4b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8f4b-115">Description</span></span>                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8f4b-116"><dt>**FILEOP \_ NEWPATH**</dt></span><span class="sxs-lookup"><span data-stu-id="f8f4b-116"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="f8f4b-117">El medio está presente y el archivo solicitado está disponible en la ruta de acceso especificada en el búfer señalado por *parám2*.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-117">The media is present and the requested file is available at the path specified in the buffer pointed to by *Param2*.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="f8f4b-118"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="f8f4b-118"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="f8f4b-119">Omitir el archivo solicitado</span><span class="sxs-lookup"><span data-stu-id="f8f4b-119">Skip the requested file</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="f8f4b-120"><dt>**\_anulación de FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="f8f4b-120"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="f8f4b-121">Anula el procesamiento de la cola.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-121">Abort queue processing.</span></span> <span data-ttu-id="f8f4b-122">La función [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-122">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE**.</span></span> <span data-ttu-id="f8f4b-123">GetLastError devuelve información de error extendida, como \_ el error cancelado si el usuario canceló la misma.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-123">GetLastError returns extended error information, such as ERROR\_CANCELLED if the user canceled.</span></span><br/> |
| <dl> <span data-ttu-id="f8f4b-124"><dt>**FILEOP-DOIT**</dt></span><span class="sxs-lookup"><span data-stu-id="f8f4b-124"><dt>**FILEOP-DOIT**</dt></span></span> </dl>     | <span data-ttu-id="f8f4b-125">El medio está disponible.</span><span class="sxs-lookup"><span data-stu-id="f8f4b-125">The media is available.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="f8f4b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8f4b-126">Requirements</span></span>



| <span data-ttu-id="f8f4b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f4b-127">Requirement</span></span> | <span data-ttu-id="f8f4b-128">Value</span><span class="sxs-lookup"><span data-stu-id="f8f4b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f4b-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8f4b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f8f4b-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f8f4b-130">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f8f4b-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8f4b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f8f4b-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8f4b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8f4b-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8f4b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8f4b-134"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8f4b-134"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f4b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8f4b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f4b-136">Información general</span><span class="sxs-lookup"><span data-stu-id="f8f4b-136">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="f8f4b-137">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="f8f4b-137">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="f8f4b-138">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="f8f4b-138">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="f8f4b-139">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="f8f4b-139">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="f8f4b-140">**medios de origen \_**</span><span class="sxs-lookup"><span data-stu-id="f8f4b-140">**SOURCE\_MEDIA**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




