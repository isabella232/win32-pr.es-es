---
description: La notificación de FILEEXTRACTED de SPFILENOTIFY \_ se envía a una rutina de devolución de llamada de SetupIterateCabinet para indicar que un archivo se ha extraído del contenedor o que se ha producido un error en la extracción y se ha cancelado el procesamiento del archivo. cab.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Mensaje de SPFILENOTIFY_FILEEXTRACTED (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669717"
---
# <a name="spfilenotify_fileextracted-message"></a><span data-ttu-id="69469-103">SPFILENOTIFY \_ FILEEXTRACTED</span><span class="sxs-lookup"><span data-stu-id="69469-103">SPFILENOTIFY\_FILEEXTRACTED message</span></span>

<span data-ttu-id="69469-104">La notificación de **\_ FILEEXTRACTED de SPFILENOTIFY** se envía a una rutina de devolución de llamada de [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para indicar que un archivo se ha extraído del contenedor o que se ha producido un error en la extracción y se ha cancelado el procesamiento del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="69469-104">The **SPFILENOTIFY\_FILEEXTRACTED** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate either that a file was extracted from the cabinet or that an extraction failed and cabinet processing has been canceled.</span></span>


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="69469-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69469-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69469-106">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="69469-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="69469-107">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información sobre la ruta de acceso del archivo extraído.</span><span class="sxs-lookup"><span data-stu-id="69469-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains path information for the extracted file.</span></span> <span data-ttu-id="69469-108">El miembro **SourceFile** de la estructura **FILEPATHS** contiene la ruta de acceso de origen completa del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="69469-108">The **SourceFile** member of the **FILEPATHS** structure contains the full source path of the cabinet.</span></span> <span data-ttu-id="69469-109">El miembro **TargetFile** proporciona la ruta de acceso de destino completa del archivo que se va a instalar en el sistema.</span><span class="sxs-lookup"><span data-stu-id="69469-109">The **TargetFile** member supplies the full target path of the file to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="69469-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="69469-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="69469-111">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="69469-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69469-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69469-112">Return value</span></span>

<span data-ttu-id="69469-113">La rutina de devolución de llamada del archivo. cab debe devolver uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="69469-113">The cabinet callback routine should return one of the following values.</span></span>



| <span data-ttu-id="69469-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="69469-114">Return code</span></span>                                                                               | <span data-ttu-id="69469-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="69469-115">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="69469-116"><dt>**SIN \_ errores**</dt></span><span class="sxs-lookup"><span data-stu-id="69469-116"><dt>**NO\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="69469-117">No se encontró ningún error y continúe procesando el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="69469-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="69469-118"><dt>**ERROR \_ XXX**</dt></span><span class="sxs-lookup"><span data-stu-id="69469-118"><dt>**ERROR\_XXX**</dt></span></span> </dl> | <span data-ttu-id="69469-119">Se produjo un error del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="69469-119">An error of the specified type occurred.</span></span> <span data-ttu-id="69469-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) devolverá cero.</span><span class="sxs-lookup"><span data-stu-id="69469-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) will return zero.</span></span> <span data-ttu-id="69469-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devolverá el código de error especificado.</span><span class="sxs-lookup"><span data-stu-id="69469-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the specified error code.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="69469-122">No se ha proporcionado ninguna rutina de devolución de llamada de archivador predeterminada con la API de instalación.</span><span class="sxs-lookup"><span data-stu-id="69469-122">There is no default cabinet callback routine supplied with the Setup API.</span></span> <span data-ttu-id="69469-123">La aplicación de instalación debe proporcionar una rutina de devolución de llamada para controlar las notificaciones enviadas por la función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="69469-123">Your setup application should supply a callback routine to handle the notifications sent by the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="69469-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69469-124">Requirements</span></span>



| <span data-ttu-id="69469-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="69469-125">Requirement</span></span> | <span data-ttu-id="69469-126">Value</span><span class="sxs-lookup"><span data-stu-id="69469-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69469-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69469-127">Minimum supported client</span></span><br/> | <span data-ttu-id="69469-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="69469-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="69469-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69469-129">Minimum supported server</span></span><br/> | <span data-ttu-id="69469-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="69469-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="69469-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="69469-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="69469-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="69469-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69469-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="69469-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69469-134">Información general</span><span class="sxs-lookup"><span data-stu-id="69469-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="69469-135">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="69469-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="69469-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="69469-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="69469-137">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="69469-137">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

