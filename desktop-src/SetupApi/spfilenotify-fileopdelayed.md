---
description: '\_SetupInstallFileEx o SetupCommitFileQueue envía la notificación SPFILENOTIFY FILEOPDELAYED a una rutina de devolución de llamada cuando se retrasa una operación de archivo porque el archivo estaba en uso. La operación se procesará la próxima vez que se reinicie el sistema.'
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Mensaje de SPFILENOTIFY_FILEOPDELAYED (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908810"
---
# <a name="spfilenotify_fileopdelayed-message"></a><span data-ttu-id="39649-104">SPFILENOTIFY \_ FILEOPDELAYED</span><span class="sxs-lookup"><span data-stu-id="39649-104">SPFILENOTIFY\_FILEOPDELAYED message</span></span>

<span data-ttu-id="39649-105">[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) o [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) envía la notificación **SPFILENOTIFY \_ FILEOPDELAYED** a una rutina de devolución de llamada cuando se retrasa una operación de archivo porque el archivo estaba en uso.</span><span class="sxs-lookup"><span data-stu-id="39649-105">The **SPFILENOTIFY\_FILEOPDELAYED** notification is sent by [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) or [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to a callback routine when a file operation was delayed because the file was in use.</span></span> <span data-ttu-id="39649-106">La operación se procesará la próxima vez que se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="39649-106">The operation will be processed the next time the system is rebooted.</span></span>


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="39649-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39649-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39649-108">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="39649-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="39649-109">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="39649-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

<span data-ttu-id="39649-110">Si la operación retrasada es una operación de copia de archivos, la estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="39649-110">If the delayed operation is a file copy operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="39649-111">Miembro FILEPATHS</span><span class="sxs-lookup"><span data-stu-id="39649-111">FILEPATHS member</span></span> | <span data-ttu-id="39649-112">Value</span><span class="sxs-lookup"><span data-stu-id="39649-112">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="39649-113">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="39649-113">**Win32Error**</span></span>   | <span data-ttu-id="39649-114">SIN \_ errores</span><span class="sxs-lookup"><span data-stu-id="39649-114">NO\_ERROR</span></span>                            |
| <span data-ttu-id="39649-115">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="39649-115">**Flags**</span></span>        | <span data-ttu-id="39649-116">copia de FILEOP \_</span><span class="sxs-lookup"><span data-stu-id="39649-116">FILEOP\_COPY</span></span>                         |
| <span data-ttu-id="39649-117">**Origen**</span><span class="sxs-lookup"><span data-stu-id="39649-117">**Source**</span></span>       | <span data-ttu-id="39649-118">Ruta de acceso completa del archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="39649-118">Full path of the temporary file.</span></span>     |
| <span data-ttu-id="39649-119">**Target**</span><span class="sxs-lookup"><span data-stu-id="39649-119">**Target**</span></span>       | <span data-ttu-id="39649-120">Ruta de acceso completa del archivo de destino real.</span><span class="sxs-lookup"><span data-stu-id="39649-120">Full path of the actual target file.</span></span> |



 

<span data-ttu-id="39649-121">Este archivo temporal se copiará en el directorio de destino cuando se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="39649-121">This temporary file will be copied to the target directory when the system is rebooted.</span></span> <span data-ttu-id="39649-122">Las funciones de configuración generan automáticamente una ruta de acceso para el archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="39649-122">The setup functions automatically generate a path for the temporary file.</span></span>

<span data-ttu-id="39649-123">Si la operación retrasada es una operación de eliminación de archivo, la estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="39649-123">If the delayed operation is a file delete operation, the [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure contains the following information.</span></span>



| <span data-ttu-id="39649-124">Miembro FILEPATHS</span><span class="sxs-lookup"><span data-stu-id="39649-124">FILEPATHS member</span></span> | <span data-ttu-id="39649-125">Value</span><span class="sxs-lookup"><span data-stu-id="39649-125">Value</span></span>                                |
|------------------|--------------------------------------|
| <span data-ttu-id="39649-126">**Win32Error**</span><span class="sxs-lookup"><span data-stu-id="39649-126">**Win32Error**</span></span>   | <span data-ttu-id="39649-127">SIN \_ errores</span><span class="sxs-lookup"><span data-stu-id="39649-127">NO\_ERROR</span></span>                            |
| <span data-ttu-id="39649-128">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="39649-128">**Flags**</span></span>        | <span data-ttu-id="39649-129">FILEOP \_ eliminar</span><span class="sxs-lookup"><span data-stu-id="39649-129">FILEOP\_DELETE</span></span>                       |
| <span data-ttu-id="39649-130">**Origen**</span><span class="sxs-lookup"><span data-stu-id="39649-130">**Source**</span></span>       | <span data-ttu-id="39649-131">NULL</span><span class="sxs-lookup"><span data-stu-id="39649-131">NULL</span></span>                                 |
| <span data-ttu-id="39649-132">**Target**</span><span class="sxs-lookup"><span data-stu-id="39649-132">**Target**</span></span>       | <span data-ttu-id="39649-133">Ruta de acceso completa del archivo que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="39649-133">Full path of the file to be deleted.</span></span> |



 

</dd> <dt>

<span data-ttu-id="39649-134">*Param2*</span><span class="sxs-lookup"><span data-stu-id="39649-134">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="39649-135">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="39649-135">Is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39649-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39649-136">Return value</span></span>

<span data-ttu-id="39649-137">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="39649-137">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="39649-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39649-138">Requirements</span></span>



| <span data-ttu-id="39649-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="39649-139">Requirement</span></span> | <span data-ttu-id="39649-140">Value</span><span class="sxs-lookup"><span data-stu-id="39649-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39649-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39649-141">Minimum supported client</span></span><br/> | <span data-ttu-id="39649-142">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="39649-142">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="39649-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39649-143">Minimum supported server</span></span><br/> | <span data-ttu-id="39649-144">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="39649-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39649-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39649-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="39649-146"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39649-146"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39649-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="39649-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39649-148">Información general</span><span class="sxs-lookup"><span data-stu-id="39649-148">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="39649-149">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="39649-149">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="39649-150">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="39649-150">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="39649-151">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="39649-151">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="39649-152">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="39649-152">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="39649-153">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="39649-153">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="39649-154">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="39649-154">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




