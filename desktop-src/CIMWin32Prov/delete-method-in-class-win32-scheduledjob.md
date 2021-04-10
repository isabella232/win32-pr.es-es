---
description: La eliminación&\# 8194; El método de clase WMI elimina un trabajo programado.
ms.assetid: 064ff3f8-6d41-4f8d-a511-6c051bb48a5b
ms.tgt_platform: multiple
title: Método Delete de la clase Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd375c3da85bd72bddfc97ed3f57e52103578441
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153567"
---
# <a name="delete-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="65fde-103">Método Delete de la \_ clase Win32 ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="65fde-103">Delete method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="65fde-104">El método **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) elimina un trabajo programado.</span><span class="sxs-lookup"><span data-stu-id="65fde-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a scheduled job.</span></span>

<span data-ttu-id="65fde-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="65fde-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="65fde-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="65fde-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="65fde-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65fde-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="65fde-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65fde-108">Parameters</span></span>

<span data-ttu-id="65fde-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="65fde-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65fde-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65fde-110">Return value</span></span>

<span data-ttu-id="65fde-111">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="65fde-111">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="65fde-112">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="65fde-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="65fde-113">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="65fde-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="65fde-114">**Completado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="65fde-114">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="65fde-115">0</span><span class="sxs-lookup"><span data-stu-id="65fde-115">0</span></span>

<span data-ttu-id="65fde-116">Se aceptó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="65fde-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="65fde-117">**No admitido**</span><span class="sxs-lookup"><span data-stu-id="65fde-117">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="65fde-118">1</span><span class="sxs-lookup"><span data-stu-id="65fde-118">1</span></span>

<span data-ttu-id="65fde-119">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="65fde-119">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="65fde-120">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="65fde-120">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="65fde-121">2</span><span class="sxs-lookup"><span data-stu-id="65fde-121">2</span></span>

<span data-ttu-id="65fde-122">El usuario no tenía el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="65fde-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="65fde-123">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="65fde-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="65fde-124">8</span><span class="sxs-lookup"><span data-stu-id="65fde-124">8</span></span>

<span data-ttu-id="65fde-125">Proceso interactivo.</span><span class="sxs-lookup"><span data-stu-id="65fde-125">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="65fde-126">**No se encuentra la ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="65fde-126">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="65fde-127">9</span><span class="sxs-lookup"><span data-stu-id="65fde-127">9</span></span>

<span data-ttu-id="65fde-128">No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="65fde-128">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="65fde-129">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="65fde-129">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="65fde-130">21</span><span class="sxs-lookup"><span data-stu-id="65fde-130">21</span></span>

<span data-ttu-id="65fde-131">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="65fde-131">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="65fde-132">**Servicio no iniciado**</span><span class="sxs-lookup"><span data-stu-id="65fde-132">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="65fde-133">22</span><span class="sxs-lookup"><span data-stu-id="65fde-133">22</span></span>

<span data-ttu-id="65fde-134">La cuenta con la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="65fde-134">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="65fde-135">**Otros**</span><span class="sxs-lookup"><span data-stu-id="65fde-135">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="65fde-136">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="65fde-136">23 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65fde-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65fde-137">Requirements</span></span>



| <span data-ttu-id="65fde-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="65fde-138">Requirement</span></span> | <span data-ttu-id="65fde-139">Value</span><span class="sxs-lookup"><span data-stu-id="65fde-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65fde-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65fde-140">Minimum supported client</span></span><br/> | <span data-ttu-id="65fde-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65fde-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65fde-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65fde-142">Minimum supported server</span></span><br/> | <span data-ttu-id="65fde-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65fde-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65fde-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="65fde-144">Namespace</span></span><br/>                | <span data-ttu-id="65fde-145">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="65fde-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65fde-146">MOF</span><span class="sxs-lookup"><span data-stu-id="65fde-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65fde-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65fde-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65fde-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65fde-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65fde-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65fde-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65fde-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="65fde-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="65fde-151">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65fde-151">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="65fde-152">**Win32 \_ ScheduledJob**</span><span class="sxs-lookup"><span data-stu-id="65fde-152">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

